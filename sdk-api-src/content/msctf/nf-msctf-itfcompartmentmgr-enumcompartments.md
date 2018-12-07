---
UID: NF:msctf.ITfCompartmentMgr.EnumCompartments
title: ITfCompartmentMgr::EnumCompartments
author: windows-sdk-content
description: The ITfCompartmentMgr::EnumCompartments method obtains an enumerator that contains the GUID of the compartments within the compartment manager.
old-location: tsf\itfcompartmentmgr_enumcompartments.htm
tech.root: TSF
ms.assetid: d8c90637-dd6d-425f-9d5d-44c7dbfcf8a5
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumCompartments, EnumCompartments method [Text Services Framework], EnumCompartments method [Text Services Framework],ITfCompartmentMgr interface, ITfCompartmentMgr interface [Text Services Framework],EnumCompartments method, ITfCompartmentMgr.EnumCompartments, ITfCompartmentMgr::EnumCompartments, _tsf_itfcompartmentmgr_enumcompartments_ref, msctf/ITfCompartmentMgr::EnumCompartments, tsf.itfcompartmentmgr_enumcompartments
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITfCompartmentMgr.EnumCompartments
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCompartmentMgr::EnumCompartments


## -description


The <b>ITfCompartmentMgr::EnumCompartments</b> method obtains an enumerator that contains the GUID of the compartments within the compartment manager.


## -parameters




### -param ppEnum [out]

Pointer to an <b>IEnumGUID</b> interface pointer that receives the enumerator object.


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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppcEnum</i> is invalid.

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
 



