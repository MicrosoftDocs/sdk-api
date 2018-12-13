---
UID: NF:ctfutb.ITfLangBarItemBitmapButton.GetText
title: ITfLangBarItemBitmapButton::GetText
author: windows-sdk-content
description: ITfLangBarItemBitmapButton::GetText method
old-location: tsf\itflangbaritembitmapbutton_gettext.htm
tech.root: TSF
ms.assetid: ac37ea79-59bb-44c1-aace-b3c0dccfd377
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetText, GetText method [Text Services Framework], GetText method [Text Services Framework],ITfLangBarItemBitmapButton interface, ITfLangBarItemBitmapButton interface [Text Services Framework],GetText method, ITfLangBarItemBitmapButton.GetText, ITfLangBarItemBitmapButton::GetText, _tsf_itflangbaritembitmapbutton_gettext_ref, ctfutb/ITfLangBarItemBitmapButton::GetText, tsf.itflangbaritembitmapbutton_gettext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemBitmapButton.GetText
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemBitmapButton::GetText


## -description




## -parameters




### -param pbstrText [out]

Pointer to a <b>BSTR</b> value that receives the string for the language bar item. This string must be allocated using the <a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> function. The caller must free this buffer when it is no longer required by calling <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pbstrText</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/29fcc913-fcc7-4321-918b-2c354dd751ff">ITfLangBarItemBitmapButton</a>



<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

