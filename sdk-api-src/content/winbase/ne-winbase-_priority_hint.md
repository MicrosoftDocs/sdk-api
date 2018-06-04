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

# _PRIORITY_HINT enumeration


## -description


Defines values that are used with the <a href="https://msdn.microsoft.com/a142b8fd-b71c-4449-a8c6-fb23715d1576">FILE_IO_PRIORITY_HINT_INFO</a> structure to specify the priority hint for a file I/O operation.


## -enum-fields




### -field IoPriorityHintVeryLow

The lowest possible priority hint level. The system uses this value for background I/O operations.


### -field IoPriorityHintLow

A low-priority hint level.


### -field IoPriorityHintNormal

A normal-priority hint level. This value is the default setting for an I/O operation.


### -field MaximumIoPriorityHintType

This value is used for validation. Supported values are less than this value.


## -see-also




<a href="https://msdn.microsoft.com/a142b8fd-b71c-4449-a8c6-fb23715d1576">FILE_IO_PRIORITY_HINT_INFO</a>



<a href="https://msdn.microsoft.com/ea4981e6-a8f1-4977-aca9-b2f53604d449">SetFileInformationByHandle</a>
 

 

