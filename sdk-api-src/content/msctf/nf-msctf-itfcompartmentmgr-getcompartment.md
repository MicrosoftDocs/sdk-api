---
UID: NF:msctf.ITfCompartmentMgr.GetCompartment
title: ITfCompartmentMgr::GetCompartment (msctf.h)
author: windows-sdk-content
description: ITfCompartmentMgr::GetCompartment method
old-location: tsf\itfcompartmentmgr_getcompartment.htm
tech.root: TSF
ms.assetid: 4f71815b-d352-4303-a3dd-180a71f9a5fe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetCompartment, GetCompartment method [Text Services Framework], GetCompartment method [Text Services Framework],ITfCompartmentMgr interface, ITfCompartmentMgr interface [Text Services Framework],GetCompartment method, ITfCompartmentMgr.GetCompartment, ITfCompartmentMgr::GetCompartment, _tsf_itfcompartmentmgr_getcompartment_ref, msctf/ITfCompartmentMgr::GetCompartment, tsf.itfcompartmentmgr_getcompartment
ms.topic: method
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
 - ITfCompartmentMgr.GetCompartment
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCompartmentMgr::GetCompartment


## -description




## -parameters




### -param rguid [in]

Contains a GUID that identifies the compartment.


### -param ppcomp [out]

Pointer to an <a href="https://msdn.microsoft.com/c9ca3eb5-1fb1-4e45-9ec4-a0296f1bc8c3">ITfCompartment</a> interface pointer that receives the compartment object.


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
<i>ppcomp</i> is invalid.

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




<a href="https://msdn.microsoft.com/7bffab6f-be40-4d3a-9342-6f81557a9656">Compartments</a>



<a href="https://msdn.microsoft.com/c9ca3eb5-1fb1-4e45-9ec4-a0296f1bc8c3">ITfCompartment
      </a>



<a href="https://msdn.microsoft.com/7cdc5c82-4aac-4ec9-b791-93cea33ba8d2">ITfCompartmentMgr</a>
 

 

