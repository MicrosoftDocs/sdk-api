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

# _CMC_DATA_INFO structure


## -description


The <b>CMC_DATA_INFO</b> structure provides a means of communicating different pieces of tagged information.


## -struct-fields




### -field cTaggedAttribute

Count of the number of elements in the <b>rgTaggedAttribute</b> member array.


### -field rgTaggedAttribute

Array of 
<a href="https://msdn.microsoft.com/4c350cda-2318-49b2-86dc-452423ceb9e3">CMC_TAGGED_ATTRIBUTE</a> structures.


### -field cTaggedRequest

Count of the number of elements in the <b>rgTaggedRequest</b> member array.


### -field rgTaggedRequest

Array of 
<a href="https://msdn.microsoft.com/425a3f14-8bc9-471d-b11c-1608db473cce">CMC_TAGGED_REQUEST</a> structures.


### -field cTaggedContentInfo

Count of the number of elements in the <b>rgTaggedContentInfo</b> member array.


### -field rgTaggedContentInfo

Array of 
<a href="https://msdn.microsoft.com/ff10dcdf-4c76-434a-a8bd-78d64ea24d23">CMC_TAGGED_CONTENT_INFO</a> structures.


### -field cTaggedOtherMsg

Count of the number of elements in the <b>rgTaggedOtherMsg</b> member array.


### -field rgTaggedOtherMsg

Array of 
<a href="https://msdn.microsoft.com/cf70c245-fe22-4c02-9cfd-07690b930585">CMC_TAGGED_OTHER_MSG</a> structures.


## -remarks



All tagged arrays are optional.



