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

# FAX_JOB_OPERATIONS_ENUM enumeration


## -description


The <b>FAX_JOB_OPERATIONS_ENUM</b> enumeration defines the operations that can be performed on a fax job. The members of this enumeration are bit values and can be used in combination.


## -enum-fields




### -field fjoVIEW

The job's TIFF image can be retrieved.


### -field fjoPAUSE

The job can be paused.


### -field fjoRESUME

The job can be resumed.


### -field fjoRESTART

The job can be restarted.


### -field fjoDELETE

The job can be deleted.


### -field fjoRECIPIENT_INFO

The job's recipient information can be retrieved.


### -field fjoSENDER_INFO

The job's sender information can be retrieved.


## -see-also




<a href="https://msdn.microsoft.com/04149d5c-e26f-4cef-9ae0-eba2a199ec51">AvailableOperations</a>



<a href="https://msdn.microsoft.com/113087c6-90dc-4bbc-ace6-b020d9949350">IFaxJobStatus::get_AvailableOperations</a>



<a href="https://msdn.microsoft.com/4d97ef95-77d0-4616-afcd-7adbc26ff3c5">IFaxOutgoingJob::get_AvailableOperations</a>
 

 

