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

# FAX_JOB_TYPE_ENUM enumeration


## -description


The <b>FAX_JOB_TYPE_ENUM</b> enumeration defines the fax job type.


## -enum-fields




### -field fjtSEND

The job is an outbound job.


### -field fjtRECEIVE

The job is an incoming job (being received through a modem).


### -field fjtROUTING

The incoming job has been received, and is now in routing mode (modem is not used). 


## -see-also




<a href="https://msdn.microsoft.com/30e91faa-7682-411c-b57d-b4d2823f47b0">IFaxJobStatus::get_JobType</a>
 

 

