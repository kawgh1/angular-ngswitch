# angular-ngswitch
angular ngswitch example
click the < > button 'display source blob' to see code

General

<div [ngSwitch="switch_expression">
	<div *ngSwitchCase="match_expression_1"> ... </div>
	<div *ngSwitchCase="match_expression_2"> ... </div>
	<div *ngSwitchCase="match_expression_3"> ... </div>
	<div *ngSwitchDefault> ... </div>
</div>


component.ts

superPower = 'wonderWoman'; // string

html

if matching a string, use "'string'"

<div [ngSwitch="superPower">
	<div *ngSwitchCase="'wonderWoman'"> ... </div>
	<div *ngSwitchCase="'superMan'"> ... </div>
	<div *ngSwitchCase="'heMan'"> ... </div>
	<div *ngSwitchCase="'spiderMan'"> ... </div>
	<div *ngSwitchDefault> ... </div>
</div>



....


component.ts

post array with objects having property of 'category'


html

<div class='author-category'>
	{{post.author}}
	<ng-container [ngSwitch]="post.category">
		<span *ngSwitchCase="'Technology'">{{post.category}}</span>
		<span *ngSwitchCase="'Science'">{{post.category}}</span>
		<span *ngSwitchCase="'Sports'">{{post.category}}</span>
	</ng-container>
</div>
