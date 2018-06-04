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

# _MINIDUMP_HANDLE_OBJECT_INFORMATION structure


## -description


Contains object-specific information for a handle.


## -struct-fields




### -field NextInfoRva

An RVA to a 
<b>MINIDUMP_HANDLE_OBJECT_INFORMATION</b> structure that specifies additional object-specific information. This member is 0 if there are no more elements in the list.


### -field InfoType

The object information type. This member is one of the values from the <a href="https://msdn.microsoft.com/255023e3-0412-42c8-ae80-eba5f00af5ff">MINIDUMP_HANDLE_OBJECT_INFORMATION_TYPE</a> enumeration.


### -field SizeOfInfo

The size of the information that follows this member, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/c0678315-391c-4ce9-aa77-a88afccf79d9">MINIDUMP_HANDLE_DESCRIPTOR_2</a>
 

 

