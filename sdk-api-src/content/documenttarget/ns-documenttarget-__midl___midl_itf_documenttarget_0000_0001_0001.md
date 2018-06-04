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

# __MIDL___MIDL_itf_documenttarget_0000_0001_0001 structure


## -description


Defines a payload to be used by the <a href="https://msdn.microsoft.com/A672E554-B117-475C-A01E-9FD4EA31621E">PackageStatusUpdated</a> method. This structure is a generic version of XPS_JOB_STATUS.


## -struct-fields




### -field JobId

The job ID.


### -field CurrentDocument

The zero-based index of the most recently processed document.


### -field CurrentPage

The zero-based index of the most recently processed page in the current document


### -field CurrentPageTotal

A running total of the number of pages that have been processed by the print job.


### -field Completion

The completion status of the job.


### -field PackageStatus

The error state of the job.


## -see-also




<a href="https://msdn.microsoft.com/A672E554-B117-475C-A01E-9FD4EA31621E">PackageStatusUpdated</a>
 

 

