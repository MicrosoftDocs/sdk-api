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

# IIsdbTSInformationDescriptor::GetRecordServiceIdByIndex


## -description


Gets a service identifier from a specified service record in an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.


## -parameters




### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">IIsdbTSInformationDescriptor::GetCountOfRecords</a>.


### -param bServiceIndex [in]

Zero-based index of the service identifier to return. To get the number of identifiers, call <a href="https://msdn.microsoft.com/bf9ec856-951e-4a75-a136-9fa6eaf9e8cd">IIsdbTSInformationDescriptor::GetRecordNumberOfServices</a>.


### -param pdwVal [out]

Receives the service identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/3c8cd33c-5c2a-48a4-9e8a-f7dd03560848">IIsdbTSInformationDescriptor</a>



<a href="https://msdn.microsoft.com/97e0d307-f41d-44e3-8f42-d00fecbcd61e">IIsdbTSInformationDescriptor::GetCountOfRecords</a>



<a href="https://msdn.microsoft.com/bf9ec856-951e-4a75-a136-9fa6eaf9e8cd">IIsdbTSInformationDescriptor::GetRecordNumberOfServices</a>
 

 

