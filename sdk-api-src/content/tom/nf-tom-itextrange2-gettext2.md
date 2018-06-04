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

# ITextRange2::GetText2


## -description


Gets the text in this range according to the specified conversion flags.


## -parameters




### -param Flags [in]

Type: <b>long</b>

The flags controlling how the text is retrieved. The flags can include a combination of the following values. Specifying a <i>Flags</i> value of 0 is the same as calling the  <a href="https://msdn.microsoft.com/8cef8a1c-7b21-43cd-a4dd-b5a579bbfdaf">ITextRange::GetText</a> method.  

<a id="tomAdjustCRLF"></a>
<a id="tomadjustcrlf"></a>
<a id="TOMADJUSTCRLF"></a>


#### tomAdjustCRLF

<a id="tomUseCRLF"></a>
<a id="tomusecrlf"></a>
<a id="TOMUSECRLF"></a>


#### tomUseCRLF

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

<a id="tomTextize"></a>
<a id="tomtextize"></a>
<a id="TOMTEXTIZE"></a>


#### tomTextize

<a id="tomAllowFinalEOP"></a>
<a id="tomallowfinaleop"></a>
<a id="TOMALLOWFINALEOP"></a>


#### tomAllowFinalEOP

<a id="tomTranslateTableCell"></a>
<a id="tomtranslatetablecell"></a>
<a id="TOMTRANSLATETABLECELL"></a>


#### tomTranslateTableCell

<a id="tomFoldMathAlpha"></a>
<a id="tomfoldmathalpha"></a>
<a id="TOMFOLDMATHALPHA"></a>


#### tomFoldMathAlpha

<a id="tomLanguageTag"></a>
<a id="tomlanguagetag"></a>
<a id="TOMLANGUAGETAG"></a>


#### tomLanguageTag


### -param pbstr [out]

Type: <b>BSTR*</b>

The text in the range.


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



This method includes the special flag <b>tomLanguageTag</b> to get the BCP-47 language tag for the range. This is an industry standard language tag which may be preferable to the language code identifier (LCID) obtained by calling <a href="https://msdn.microsoft.com/422f94bc-44ef-44db-be8c-50fe1acc2320">ITextFont::GetLanguageID</a>.




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/dd7a8a16-6cb5-40ee-8f5f-e51e68785d93">ITextRange2::SetText2</a>
 

 

