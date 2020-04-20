---
UID: NF:msctf.ITfRange.GetContext
title: ITfRange::GetContext (msctf.h)
description: ITfRange::GetContext methodhelpviewer_keywords: ["GetContext","GetContext method [Text Services Framework]","GetContext method [Text Services Framework]","ITfRange interface","ITfRange interface [Text Services Framework]","GetContext method","ITfRange.GetContext","ITfRange::GetContext","_tsf_itfrange_getcontext_ref","msctf/ITfRange::GetContext","tsf.itfrange_getcontext"]
old-location: tsf\itfrange_getcontext.htm
tech.root: TSF
ms.assetid: c3ba1424-f6c9-41f1-b815-4c315bfba868
ms.date: 12/05/2018
ms.keywords: GetContext, GetContext method [Text Services Framework], GetContext method [Text Services Framework],ITfRange interface, ITfRange interface [Text Services Framework],GetContext method, ITfRange.GetContext, ITfRange::GetContext, _tsf_itfrange_getcontext_ref, msctf/ITfRange::GetContext, tsf.itfrange_getcontext
f1_keywords:
- msctf/ITfRange.GetContext
dev_langs:
- c++
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
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
- ITfRange.GetContext
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfRange::GetContext


## -description

Obtains the context object to which the range belongs.

## -parameters




### -param ppContext [out]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext</a> interface pointer that receives the context object that the range belongs to.


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
<i>ppContext</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcontext">ITfContext
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfrange">ITfRange</a>
 

 

