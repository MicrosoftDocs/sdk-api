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

# IIsdbComponentGroupDescriptor::GetRecordCAUnitComponentTag


## -description


Gets the tag that identifies a component record in an Integrated Services Digital Broadcasting (ISDB) component group descriptor.


## -parameters




### -param bRecordIndex [in]

Specifies the component record number,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/b5b8334c-a3f1-42f7-81c9-d0c461e17f25">IIsdbComponentGroupDescriptor::GetCountOfRecords</a>
  method to get the number of records in the extended event descriptor.


### -param bCAUnitIndex [in]

Specifies the conditional access unit number within the component group,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/239d952f-908d-4aa9-86c0-f58f7616987f">IIsdbComponentGroupDescriptor::GetRecordNumberOfCAUnit</a>
  method to get the number of records in the extended event descriptor.


### -param bComponentIndex [in]

Specifies the component within the component group,
  indexed from zero. Call the <a href="https://msdn.microsoft.com/2656ecfd-84a1-43cb-8fa3-a188f9176c01">IIsdbComponentGroupDescriptor::GetRecordCAUnitNumberOfComponents</a>
  method to get the number of components for the conditional access unit given by the <i>bCAUnitIndex</i> parameter.


### -param pbVal [out]

Receives the component tag value.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/54ba8ca6-712f-46a1-9ed1-2b20ef8539ba">IIsdbComponentGroupDescriptor</a>
 

 

