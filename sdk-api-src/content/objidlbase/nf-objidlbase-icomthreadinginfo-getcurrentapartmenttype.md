---
UID: NF:objidlbase.IComThreadingInfo.GetCurrentApartmentType
title: IComThreadingInfo::GetCurrentApartmentType (objidlbase.h)
description: Retrieves the type of apartment in which the caller is executing.
helpviewer_keywords: ["GetCurrentApartmentType","GetCurrentApartmentType method [COM]","GetCurrentApartmentType method [COM]","IComThreadingInfo interface","IComThreadingInfo interface [COM]","GetCurrentApartmentType method","IComThreadingInfo.GetCurrentApartmentType","IComThreadingInfo::GetCurrentApartmentType","_com_icomthreadinginfo_getcurrentapartmenttype","com.icomthreadinginfo_getcurrentapartmenttype","objidlbase/IComThreadingInfo::GetCurrentApartmentType"]
old-location: com\icomthreadinginfo_getcurrentapartmenttype.htm
tech.root: com
ms.assetid: 59cb216f-818c-4189-b77b-984961889a62
ms.date: 12/05/2018
ms.keywords: GetCurrentApartmentType, GetCurrentApartmentType method [COM], GetCurrentApartmentType method [COM],IComThreadingInfo interface, IComThreadingInfo interface [COM],GetCurrentApartmentType method, IComThreadingInfo.GetCurrentApartmentType, IComThreadingInfo::GetCurrentApartmentType, _com_icomthreadinginfo_getcurrentapartmenttype, com.icomthreadinginfo_getcurrentapartmenttype, objidlbase/IComThreadingInfo::GetCurrentApartmentType
f1_keywords:
- objidlbase/IComThreadingInfo.GetCurrentApartmentType
dev_langs:
- c++
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- objidlbase.h
api_name:
- IComThreadingInfo.GetCurrentApartmentType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComThreadingInfo::GetCurrentApartmentType


## -description


Retrieves the type of apartment in which the caller is executing.


## -parameters




### -param pAptType [out]

A points to an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/ne-objidl-apttype">APTTYPE</a> enumeration value that characterizes the caller's apartment.


## -returns



This method can return the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The caller is not executing in an apartment.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-icomthreadinginfo">IComThreadingInfo</a>
 

 

