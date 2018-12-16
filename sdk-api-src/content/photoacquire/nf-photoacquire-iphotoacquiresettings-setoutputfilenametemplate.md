---
UID: NF:photoacquire.IPhotoAcquireSettings.SetOutputFilenameTemplate
title: IPhotoAcquireSettings::SetOutputFilenameTemplate
author: windows-sdk-content
description: The SetOutputFilenameTemplate method specifies a format string (template) that specifies the format of file names.
old-location: picacq\iphotoacquiresettings_setoutputfilenametemplate.htm
tech.root: acquisition
ms.assetid: 28eaeee4-05eb-4d51-9e21-937481bc7703
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPhotoAcquireSettings interface [Picture Acquisition],SetOutputFilenameTemplate method, IPhotoAcquireSettings.SetOutputFilenameTemplate, IPhotoAcquireSettings::SetOutputFilenameTemplate, IPhotoAcquireSettingsSetOutputFilenameTemplate, SetOutputFilenameTemplate, SetOutputFilenameTemplate method [Picture Acquisition], SetOutputFilenameTemplate method [Picture Acquisition],IPhotoAcquireSettings interface, photoacquire/IPhotoAcquireSettings::SetOutputFilenameTemplate, picacq.iphotoacquiresettings_setoutputfilenametemplate
ms.topic: method
req.header: photoacquire.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PhotoAcquireUID.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PhotoAcquireUID.lib
 - PhotoAcquireUID.dll
api_name:
 - IPhotoAcquireSettings.SetOutputFilenameTemplate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPhotoAcquireSettings::SetOutputFilenameTemplate


## -description



The <code>SetOutputFilenameTemplate</code> method specifies a format string (template) that specifies the format of file names.




## -parameters




### -param pszTemplate [in]

Pointer to a null-terminated string containing the format string.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Format strings contain a mix of path literals and tokens. A format string looks like the following:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
$(MyPicturesFolder)\$(DateAcquired), $(EventName)\$(EventName) $(SequenceNumber).$(OriginalExtension)
</pre>
</td>
</tr>
</table></span></div>
The token format looks like the following, where <code>OptionalPrefix</code> and <code>OptionSuffix</code> are suppressed if the replacement for the <code>TokenIdentifier</code> yields a zero-length string:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
$([OptionalPrefix]TokenIdentifier:SubToken[OptionalSuffix]|AlternateString)
</pre>
</td>
</tr>
</table></span></div>
The caret ("^") is an escape character, so "^$" would yield "$" in the final path.

Parentheses and brackets are not allowed as literals within tokens, but can be used outside of tokens. This means you cannot use "[", "]", "(", or ")" within the <code>OptionalString</code> sub-token unless they are escaped with a caret ("^").

There are a few different classes of tokens, including the following:

<b>SHGetSpecialFolder</b> variables such as the following. These must be the first token, and can only occur once, at most:

<ul>
<li><code>MyPicturesFolder</code></li>
<li><code>MyDocumentsFolder</code></li>
</ul>
Session variables such as the following:

<ul>
<li><code>SequenceNumber</code> (The sequence number is used to avoid filename collisions; if it exists, it must be in the file name portion of the path.)</li>
<li><code>DateAcquired</code></li>
<li><code>EventName</code></li>
<li><code>UserName</code></li>
<li><code>MachineName</code></li>
</ul>
File and metadata variables such as the following:

<ul>
<li><code>DateTaken</code></li>
<li><code>OriginalFilename</code></li>
<li><code>OriginalExtension</code></li>
<li><code>CameraModel</code></li>
<li><code>Width</code></li>
<li><code>Height</code></li>
</ul>
Since these tokens are not intended to be visible to users, they will not be localized. For example, <code>$(DateTaken)</code> will be the same on all versions of Microsoft Windows, regardless of locale or language settings.

As an example, suppose <code>EventName</code> is "Meghan's Birthday" and the naming pattern is as follows:

<pre class="syntax" xml:space="preserve"><code>
$(MyPicturesFolder)\$(DateAcquired)$([, ]EventName)\$(EventName[ ])$(SequenceNumber).$(OriginalExtension)
</code></pre>
The resulting files would be named as follows:

C:\Documents and Settings\shauniv\My Documents\My Pictures\2003-11-14, Meghan's Birthday\Meghan's Birthday 001.jpg

C:\Documents and Settings\shauniv\My Documents\My Pictures\2003-11-14, Meghan's Birthday\Meghan's Birthday 002.jpg

C:\Documents and Settings\shauniv\My Documents\My Pictures\2003-11-14, Meghan's Birthday\Meghan's Birthday 003.jpg

C:\Documents and Settings\shauniv\My Documents\My Pictures\2003-11-14, Meghan's Birthday\Meghan's Birthday 004.jpg




## -see-also




<a href="https://msdn.microsoft.com/ca36e3f9-74ad-4704-adeb-d3102668da30">GetOutputFilenameTemplate</a>



<a href="https://msdn.microsoft.com/c86d0c97-f9ef-4a73-865b-8aea7972193b">IPhotoAcquireSettings Interface</a>
 

 

