---
UID: NF:objidlbase.IComThreadingInfo.GetCurrentApartmentType
title: IComThreadingInfo::GetCurrentApartmentType method
author: windows-driver-content
description: Retrieves the type of apartment in which the caller is executing.
old-location: com\icomthreadinginfo_getcurrentapartmenttype.htm
old-project: com
ms.assetid: 59cb216f-818c-4189-b77b-984961889a62
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: GetCurrentApartmentType method [COM], GetCurrentApartmentType method [COM], IComThreadingInfo interface, GetCurrentApartmentType,IComThreadingInfo.GetCurrentApartmentType, IComThreadingInfo, IComThreadingInfo interface [COM], GetCurrentApartmentType method, IComThreadingInfo::GetCurrentApartmentType, _com_icomthreadinginfo_getcurrentapartmenttype, com.icomthreadinginfo_getcurrentapartmenttype, objidlbase/IComThreadingInfo::GetCurrentApartmentType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	objidlbase.h
api_name:
-	IComThreadingInfo.GetCurrentApartmentType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IComThreadingInfo::GetCurrentApartmentType method


## -description


Retrieves the type of apartment in which the caller is executing.


## -parameters




### -param pAptType [out]

A points to an <a href="https://msdn.microsoft.com/eae95b1f-3883-4334-aa7e-84e71e05fb24">APTTYPE</a> enumeration value that characterizes the caller's apartment.


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




<a href="https://msdn.microsoft.com/fa4c7d82-ec5d-43d6-914e-bba60ad19aa2">IComThreadingInfo</a>
 

 

