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

# _gettextlengthex structure


## -description


Contains information about how the text length of a rich edit control should be calculated. This structure is passed in the <b>wParam</b> in the <a href="https://msdn.microsoft.com/42c89b7b-e48d-4517-9993-ce58ff9e4e40">EM_GETTEXTLENGTHEX</a> message.


## -struct-fields




### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

Value specifying the method to be used in determining the text length. This member can be one or more of the following values (some values are mutually exclusive). 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="GTL_DEFAULT"></a><a id="gtl_default"></a><dl>
<dt><b>GTL_DEFAULT</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of characters. This is the default.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_USECRLF"></a><a id="gtl_usecrlf"></a><dl>
<dt><b>GTL_USECRLF</b></dt>
</dl>
</td>
<td width="60%">
Computes the answer by using CR/LFs at the end of paragraphs.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_PRECISE"></a><a id="gtl_precise"></a><dl>
<dt><b>GTL_PRECISE</b></dt>
</dl>
</td>
<td width="60%">
Computes a precise answer. This approach could necessitate a conversion and thereby take longer. This flag cannot be used with the GTL_CLOSE flag. E_INVALIDARG will be returned if both are used.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_CLOSE"></a><a id="gtl_close"></a><dl>
<dt><b>GTL_CLOSE</b></dt>
</dl>
</td>
<td width="60%">
Computes an approximate (close) answer. It is obtained quickly and can be used to set the buffer size. This flag cannot be used with the GTL_PRECISE flag. E_INVALIDARG will be returned if both are used.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_NUMCHARS"></a><a id="gtl_numchars"></a><dl>
<dt><b>GTL_NUMCHARS</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of characters. This flag cannot be used with the GTL_NUMBYTES flag. E_INVALIDARG will be returned if both are used.

</td>
</tr>
<tr>
<td width="40%"><a id="GTL_NUMBYTES"></a><a id="gtl_numbytes"></a><dl>
<dt><b>GTL_NUMBYTES</b></dt>
</dl>
</td>
<td width="60%">
Returns the number of bytes. This flag cannot be used with the GTL_NUMCHARS flag. E_INVALIDARG will be returned if both are used.

</td>
</tr>
</table>
 


### -field codepage

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Code page used in the translation. It is CP_ACP for ANSI Code Page and 1200 for Unicode. 


## -see-also




<a href="https://msdn.microsoft.com/42c89b7b-e48d-4517-9993-ce58ff9e4e40">EM_GETTEXTLENGTHEX</a>
 

 

