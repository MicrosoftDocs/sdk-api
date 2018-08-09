---
UID: NF:ctfutb.ITfLangBarItemButton.GetText
title: ITfLangBarItemButton::GetText
author: windows-sdk-content
description: ITfLangBarItemButton::GetText method
old-location: tsf\itflangbaritembutton_gettext.htm
old-project: TSF
ms.assetid: 9c50f934-d968-4a3d-8455-8923d98b926e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetText, GetText method [Text Services Framework], GetText method [Text Services Framework],ITfLangBarItemButton interface, ITfLangBarItemButton interface [Text Services Framework],GetText method, ITfLangBarItemButton.GetText, ITfLangBarItemButton::GetText, _tsf_itflangbaritembutton_gettext_ref, ctfutb/ITfLangBarItemButton::GetText, tsf.itflangbaritembutton_gettext
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TfLBIClick
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfLangBarItemButton.GetText
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemButton::GetText


## -description




## -parameters




### -param pbstrText [out]

Pointer to a <b>BSTR</b> that receives the string for the language bar item. This string must be allocated using the <a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> function. The caller must free this buffer when it is no longer required by calling <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>.


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




<a href="https://msdn.microsoft.com/098a8cdc-ff34-4729-9b34-279c499d40a8">ITfLangBarItemButton</a>



<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

