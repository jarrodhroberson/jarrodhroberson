### Hi there 👋

#### 👷 Check out what I'm currently working on
{{range recentContributions 10}}
- [{{.Repo.Name}}]({{.Repo.URL}}) - {{.Repo.Description}} ({{humanize .OccurredAt}})
{{- end}}
[... and other Github related content ...] 

#### 💬 Feedback

Say Hello, I don't bite!

#### 📫 How to reach me

- Fediverse: https://mastodon.social/@...
- Blog: https://vertigrated.com/blog

#### 📜 My recent blog posts
{{range rss "https://medium.com/feed/@<jarrodhroberson>" 5}}
- [{{.Title}}]({{.URL}}) ({{humanize .PublishedAt}})
{{- end}}

## 📜 🇫🇷 My recent videos
<img src="https://img.shields.io/youtube/channel/subscribers/UCzdX32OIhpfrdxQRhN2s98w?style=for-the-badge"></img>
<table>
{{range rss "https://www.youtube.com/feeds/videos.xml?channel_id=UCzdX32OIhpfrdxQRhN2s98w" 10}}
<tr>
  <td>
    <img src="https://img.youtube.com/vi/{{slice .URL 32}}/default.jpg"></img>
  </td>
  <td>
    <a href="{{.URL}}">{{.Title}}</a> ({{humanize .PublishedAt}})  
    <br/>
    <img src="https://img.shields.io/youtube/views/{{slice .URL 32}}?style=flat-square"> </img>
  </td>
</tr>
{{- end}}
</table>