---
UID: NF:msctf.ITfThreadMgr.GetGlobalCompartment
title: ITfThreadMgr::GetGlobalCompartment (msctf.h)
description: ITfThreadMgr::GetGlobalCompartment methodhelpviewer_keywords: ["GetGlobalCompartment","GetGlobalCompartment method [Text Services Framework]","GetGlobalCompartment method [Text Services Framework]","ITfThreadMgr interface","ITfThreadMgr interface [Text Services Framework]","GetGlobalCompartment method","ITfThreadMgr.GetGlobalCompartment","ITfThreadMgr::GetGlobalCompartment","_tsf_itfthreadmgr_getglobalcompartment_ref","msctf/ITfThreadMgr::GetGlobalCompartment","tsf.itfthreadmgr_getglobalcompartment"]
old-location: tsf\itfthreadmgr_getglobalcompartment.htm
tech.root: TSF
ms.assetid: 801e2c3a-0445-4630-83ba-55f51ef2704e
ms.date: 12/05/2018
ms.keywords: GetGlobalCompartment, GetGlobalCompartment method [Text Services Framework], GetGlobalCompartment method [Text Services Framework],ITfThreadMgr interface, ITfThreadMgr interface [Text Services Framework],GetGlobalCompartment method, ITfThreadMgr.GetGlobalCompartment, ITfThreadMgr::GetGlobalCompartment, _tsf_itfthreadmgr_getglobalcompartment_ref, msctf/ITfThreadMgr::GetGlobalCompartment, tsf.itfthreadmgr_getglobalcompartment
f1_keywords:
- msctf/ITfThreadMgr.GetGlobalCompartment
dev_langs:
- c++
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
- ITfThreadMgr.GetGlobalCompartment
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfThreadMgr::GetGlobalCompartment


## -description

Obtains the global compartment manager object.

## -parameters




### -param ppCompMgr [out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcompartmentmgr">ITfCompartmentMgr</a> interface that receives the global compartment manager.


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
<i>ppCompMgr</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcompartmentmgr">ITfCompartmentMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfthreadmgr">ITfThreadMgr</a>
 

 

