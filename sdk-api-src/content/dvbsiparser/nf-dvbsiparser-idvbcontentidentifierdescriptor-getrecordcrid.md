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

# IDvbContentIdentifierDescriptor::GetRecordCrid


## -description


Gets the content reference identifier (CRID) from a Digital Video Broadcast (DVB) content identifier descriptor.  


## -parameters




### -param bRecordIndex [in]

Zero-based index of the service record to return. To get the number of service records in the descriptor, call the <a href="https://msdn.microsoft.com/cd96a052-52e6-4de7-aa44-66c2caa4d5f5">IDvbContentIdentifierDescriptor::GetCountOfRecords</a> method.


### -param pbType [out]

Receives the type of the CRID. 


### -param pbLocation [out]

Gets the location of the CRID. 


### -param pbLength [out]

Gets the number of bytes required to return the CRID.


### -param ppbBytes [out]

Pointer to a buffer that receives the CRID. The caller is responsible for freeing this memory.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bdd15b6f-2f1e-438a-a2fd-f3fa4df2a9fd">IDvbContentIdentifierDescriptor</a>



<a href="https://msdn.microsoft.com/cd96a052-52e6-4de7-aa44-66c2caa4d5f5">IDvbContentIdentifierDescriptor::GetCountOfRecords</a>
 

 

