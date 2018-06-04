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

# ITextRange2::SetText2


## -description


Sets the text of this range.


## -parameters




### -param Flags [in]

Type: <b>long</b>

Flags controlling how the text is inserted in the range. The flag can be one of the following values:

<a id="tomUnicodeBiDi"></a>
<a id="tomunicodebidi"></a>
<a id="TOMUNICODEBIDI"></a>


#### tomUnicodeBiDi

<a id="tomMathCFCheck"></a>
<a id="tommathcfcheck"></a>
<a id="TOMMATHCFCHECK"></a>


#### tomMathCFCheck

<a id="tomUnlink"></a>
<a id="tomunlink"></a>
<a id="TOMUNLINK"></a>


#### tomUnlink

<a id="tomUnhide"></a>
<a id="tomunhide"></a>
<a id="TOMUNHIDE"></a>


#### tomUnhide

<a id="tomCheckTextLimit"></a>
<a id="tomchecktextlimit"></a>
<a id="TOMCHECKTEXTLIMIT"></a>


#### tomCheckTextLimit

<a id="tomLanguageTag"></a>
<a id="tomlanguagetag"></a>
<a id="TOMLANGUAGETAG"></a>


#### tomLanguageTag


### -param bstr [in]

Type: <b>BSTR</b>

The new text.


## -returns



Type: <b>HRESULT</b>

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



If the <i>bstr</i> parameter is <b>NULL</b>, the text in the range is deleted. 

This method is similar to <a href="https://msdn.microsoft.com/26dd5c84-953c-4234-a0b4-53711990bce9">ITextRange:: SetText</a>, but lets the client specify flags that control various insertion options, including the special flag <b>tomLanguageTag</b> to get the BCP-47 language tag for the range. This is an industry standard language tag that may be preferable to <a href="https://msdn.microsoft.com/5c45a2f7-d2c3-4a7a-b5bb-b06ba59d5adf">ITextFont::SetLanguageID</a>, which uses a language code identifier (LCID).




## -see-also




<a href="https://msdn.microsoft.com/905f0967-8b99-45ed-a1cc-19d49e919a65">ITextRange2</a>



<a href="https://msdn.microsoft.com/77f39808-b39d-45bb-ba03-3a27d503fe0e">ITextRange2::GetText2</a>
 

 

