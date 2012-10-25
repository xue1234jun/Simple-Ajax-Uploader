Simple Ajax Uploader
============================

Javascript plugin for AJAX-style file uploading with progress support.

### Features ###
* Uses XMLHttpRequest and HTML5 file API with fall back to iframe method for Internet Explorer.
* Provides individual methods for XHR-supported browsers and Internet Explorer for greater control over user experience.
* Requires no external libraries.
* Fast and lightweight - only about 3.2KB when minified and gzipped.
* Tested in IE7+, Firefox 4+, Safari 4+, and Chrome.

### Getting Started ###
Include `SimpleAjaxUploader.js` into your page:

```html
	<script type="text/javascript" src="SimpleAjaxUploader.js"></script>
```

Initialize the uploader when the DOM is ready. There are three required parameters:


```javascript
var uploader = new ss.SimpleUpload({
	button: 'upload-btn',
	url: '/PathTo/UploadHandler',
	name: 'uploadfile'
});
```

### License ###
Released under the MIT license.

### Settings ###
<table>
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Default</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>button</td>
            <td>String, Element</td>
            <td>''</td>
            <td>File upload button. <strong>Required.</strong></td>
        </tr>
        <tr>
            <td>url</td>
            <td>String</td>
            <td>''</td>
            <td>Location of the server-side file upload handler. <strong>Required.</strong></td>
        </tr>		
        <tr>
            <td>name</td>
            <td>String</td>
            <td>''</td>
            <td>File upload name. <strong>Required.</strong></td>
        </tr>
        <tr>
            <td>data</td>
            <td>Object</td>
            <td>{}</td>
            <td>Additional data to be sent to the server.</td>
        </tr>
        <tr>
            <td>autoSubmit</td>
            <td>Boolean</td>
            <td>true</td>
            <td>By default, uploads commence as soon as a file is selected. Set to false to delay the upload and trigger manually.</td>
        </tr>
        <tr>
            <td>responseType</td>
            <td>String</td>
            <td>'text'</td>
            <td>The type of data you're expecting back from the server. Default is plain text. Additional option is 'json'.</td>
        </tr>		
        <tr>
            <td>debug</td>
            <td>Boolean</td>
            <td>false</td>
            <td>Setting debug to true will log progress messages and server response in the console.</td>
        </tr>		
        <tr>
            <td>hoverClass</td>
            <td>String</td>
            <td>''</td>
            <td>Class applied to upload button when mouse is hovered.</td>
        </tr>		
        <tr>
            <td>focusClass</td>
            <td>String</td>
            <td>''</td>
            <td>Class applied to upload button when focused.</td>
        </tr>	
        <tr>
            <td>disabledClass</td>
            <td>String</td>
            <td>''</td>
            <td>Class applied to button when disabled.</td>
        </tr>		
        <tr>
            <td>onChange(filename, extension)</td>
            <td>Function</td>
            <td></td>
            <td>Function to be called when user selects a file.</td>
        </tr>		
	</tbody>
</table>