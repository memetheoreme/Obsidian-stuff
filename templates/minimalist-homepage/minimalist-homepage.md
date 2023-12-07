---
document-type: dashboard
tags:
---
# H O M E

<br>

````col
```col-md
> [!menue]- HEADING 1
> ➝ &nbsp; [[NOTE A]]
> ➝ &nbsp; [[NOTE B]] 

> [!menue]- HEADING 2
> ➝ &nbsp; [[NOTE C]]
> ➝ &nbsp;  [[NOTE D]]

>[!menue]- HEADING 3
> Text description of TITLE 3
> ➝ &nbsp; [[NOTE E]]
> ➝ &nbsp; [[NOTE F]]
> ➝ &nbsp; [[NOTE G]]
```

```col-md
>[!menue]- HEADING 3
> ➝ &nbsp; [[NOTE H]]
> ➝ &nbsp; [[NOTE I]]
> ➝ &nbsp; [[NOTE J]]

> [!menue]- HEADING 4
> ➝ &nbsp; [[NOTE K]]
> ➝ &nbsp; [[NOTE L]]
> ➝ &nbsp; [[NOTE M]]

> [!menue]- HEADING 5
> ➝ &nbsp; [[NOTE N]]
> ➝ &nbsp; [[NOTE O]]

```
````

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

>[!dot-border]- Recently changed
> ```dataviewjs
> function converteTime(time){
>	// Convert from ms to minutes
>	let convertedTime = ""
>	time = time/60000; // time in minutes
>
>	if(time < 60){
>		convertedTime = `${Math.ceil(time)} minutes ago`;
>	} else if (time < 1440){
>		convertedTime = `${Math.ceil(time/60)} hours ago`
>	} else {
>		convertedTime = `${Math.ceil(time/1440)} days ago`
>	}	
>	return convertedTime
> }
>
> for (let group of dv.pages('!"_data_"').sort(k => k.file.mtime, 'desc').limit(10).groupBy(p => p.page)) {
>	dv.table(["Name", "Date Modified", ""], 
>		group.rows
>			.sort(k => k.file.mtime, 'desc')
>			.map(k => [
>			k.file.link, 
>			converteTime(Date.now()-k.file.mtime),
>			`<small>[[${k.file.path}|View →]]</small>`
>			]))}
> ```


> [!dot-border]- Active Projects 
> heheheh

<br>

**[[HOME]]** | [[NOTE]] | [[NOTE]] | [[ADD AS MANY OR AS FEW NOTES AS YOU WANT]]
