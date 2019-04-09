---
UID: NF:ctfutb.ITfLangBarItem.GetTooltipString
title: ITfLangBarItem::GetTooltipString (ctfutb.h)
author: windows-sdk-content
description: ITfLangBarItem::GetTooltipString method
old-location: tsf\itflangbaritem_gettooltipstring.htm
tech.root: TSF
ms.assetid: f0bb3c7f-c21e-443a-965a-0601de0210b5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTooltipString, GetTooltipString method [Text Services Framework], GetTooltipString method [Text Services Framework],ITfLangBarItem interface, ITfLangBarItem interface [Text Services Framework],GetTooltipString method, ITfLangBarItem.GetTooltipString, ITfLangBarItem::GetTooltipString, _tsf_itflangbaritem_gettooltipstring_ref, ctfutb/ITfLangBarItem::GetTooltipString, tsf.itflangbaritem_gettooltipstring
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
 - Msctf.dll
api_name:
 - ITfLangBarItem.GetTooltipString
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItem::GetTooltipString


## -description




## -parameters




### -param pbstrToolTip [out]

Pointer to a <b>BSTR</b> value that receives the tooltip string for the language bar item. This string must be allocated using the <a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a> function. The caller must free this buffer when it is no longer required by calling <a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>.


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
<i>pbstrToolTip</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The language bar item does not support tooltip text.

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




<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221458(v=VS.85).aspx">SysAllocString</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

