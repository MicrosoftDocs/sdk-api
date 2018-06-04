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

# IISDB_NBIT::GetRecordDescriptorByIndex


## -description



  Retrieves a descriptor for a specified record in 
  an Integrated Services Digital Broadcasting (ISDB) 
  network broadcaster information table (NBIT)
  based on the descriptor index.


## -parameters




### -param dwRecordIndex [in]

Specifies the record number, indexed from zero. 
Call the <a href="https://msdn.microsoft.com/c747278a-dea7-4772-b37d-89c1deaaf91f">IISDB_NBIT::GetCountOfRecords</a> 
 method to get the number 
of records in the NBIT.


### -param dwIndex [in]

Specifies which descriptor to retrieve, indexed from zero. 
Call the <a href="https://msdn.microsoft.com/2f4f5b5a-f03a-4b90-aa7c-2552841ba165">IISDB_NBIT::GetRecordCountOfDescriptors</a> method 
to get the number of descriptors for a particular record.


### -param ppDescriptor [out]

Pointer to the <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> interface implemented by the descriptor. The caller is responsible for freeing the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a>



<a href="https://msdn.microsoft.com/32c15a03-6683-4b22-b374-a15784696368">IISDB_NBIT</a>



<a href="https://msdn.microsoft.com/2f4f5b5a-f03a-4b90-aa7c-2552841ba165">IISDB_NBIT::GetRecordCountOfDescriptors</a>
 

 

