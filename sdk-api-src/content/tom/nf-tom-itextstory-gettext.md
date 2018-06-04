---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ITextStory::GetText


## -description


Gets the text in a story according to the specified conversion flags. 


## -parameters




### -param Flags [in]

Type: <b>long</b>

The conversion flags.


A <i>Flags</i> value of 0 retrieves text the same as <a href="https://msdn.microsoft.com/8cef8a1c-7b21-43cd-a4dd-b5a579bbfdaf">ITextRange::GetText</a>.  Other values include the following.

<a id="tomAdjustCRLF"></a>
<a id="tomadjustcrlf"></a>
<a id="TOMADJUSTCRLF"></a>


#### tomAdjustCRLF

<a id="tomAllowFinalEOP"></a>
<a id="tomallowfinaleop"></a>
<a id="TOMALLOWFINALEOP"></a>


#### tomAllowFinalEOP

<a id="tomFoldMathAlpha"></a>
<a id="tomfoldmathalpha"></a>
<a id="TOMFOLDMATHALPHA"></a>


#### tomFoldMathAlpha

<a id="tomIncludeNumbering"></a>
<a id="tomincludenumbering"></a>
<a id="TOMINCLUDENUMBERING"></a>


#### tomIncludeNumbering

<a id="tomNoHidden"></a>
<a id="tomnohidden"></a>
<a id="TOMNOHIDDEN"></a>


#### tomNoHidden

<a id="tomNoMathZoneBrackets"></a>
<a id="tomnomathzonebrackets"></a>
<a id="TOMNOMATHZONEBRACKETS"></a>


#### tomNoMathZoneBrackets

<a id="tomLanguageTag"></a>
<a id="tomlanguagetag"></a>
<a id="TOMLANGUAGETAG"></a>


#### tomLanguageTag

<a id="tomTextize"></a>
<a id="tomtextize"></a>
<a id="TOMTEXTIZE"></a>


#### tomTextize

<a id="tomTranslateTableCell"></a>
<a id="tomtranslatetablecell"></a>
<a id="TOMTRANSLATETABLECELL"></a>


#### tomTranslateTableCell

<a id="tomUseCRLF"></a>
<a id="tomusecrlf"></a>
<a id="TOMUSECRLF"></a>


#### tomUseCRLF


### -param pbstr [out]

Type: <b>BSTR*</b>

The text in the story.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Write access is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



This method is similar to using <a href="https://msdn.microsoft.com/77f39808-b39d-45bb-ba03-3a27d503fe0e">ITextRange2::GetText2</a> for a whole story, but it doesn’t require a range.




## -see-also




<a href="https://msdn.microsoft.com/8b52c6e8-c250-4cfb-979e-770df9f94010">ITextStory</a>



<a href="https://msdn.microsoft.com/9efd45ed-00f7-47e1-90e7-82a420e79bdf">ITextStory::SetText</a>
 

 

