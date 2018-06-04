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

# tag_WBEM_STATUS_TYPE enumeration


## -description


Describes the status of an asynchronous operation.


## -enum-fields




### -field WBEM_STATUS_COMPLETE

The operation has completed.


### -field WBEM_STATUS_REQUIREMENTS

Used in activating post-filtering.


### -field WBEM_STATUS_PROGRESS

The operation is still in progress.


### -field WBEM_STATUS_LOGGING_INFORMATION

Reserved for future use.


### -field WBEM_STATUS_LOGGING_INFORMATION_PROVIDER

Reserved for future use.


### -field WBEM_STATUS_LOGGING_INFORMATION_HOST

Reserved for future use.


### -field WBEM_STATUS_LOGGING_INFORMATION_REPOSITORY

Reserved for future use.


### -field WBEM_STATUS_LOGGING_INFORMATION_ESS

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/e47e8cd9-4e80-45c4-b1f0-2f68aea4eb7b">IWbemObjectSink::SetStatus</a>



<a href="https://msdn.microsoft.com/d8b55500-d84c-431b-93c6-99d1f1b845c3">IWbemServices::ExecQueryAsync</a>
 

 

