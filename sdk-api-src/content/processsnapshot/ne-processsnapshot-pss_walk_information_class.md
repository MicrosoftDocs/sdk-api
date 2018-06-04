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

# PSS_WALK_INFORMATION_CLASS enumeration


## -description


Specifies what information the <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a> function returns.


## -enum-fields




### -field PSS_WALK_AUXILIARY_PAGES

Returns a <a href="https://msdn.microsoft.com/A3D948E6-6FFE-4732-A8C7-A292FDA07D7C">PSS_AUXILIARY_PAGE_ENTRY</a> structure, which contains the address, page attributes and contents of an auxiliary copied page.


### -field PSS_WALK_VA_SPACE

Returns a <a href="https://msdn.microsoft.com/69B8F6A3-76DF-421B-B89B-73BA3254F897">PSS_VA_SPACE_ENTRY</a> structure, which contains the <a href="https://msdn.microsoft.com/library/windows/hardware/dn957515">MEMORY_BASIC_INFORMATION</a> structure for every distinct VA region.


### -field PSS_WALK_HANDLES

Returns a <a href="https://msdn.microsoft.com/F56E8C35-949A-4DEE-973F-CF24F6596036">PSS_HANDLE_ENTRY</a> structure, with information specifying the handle value, its type name, object name (if captured), basic information (if captured), and type-specific information (if captured).


### -field PSS_WALK_THREADS

Returns a <a href="https://msdn.microsoft.com/99C89DBB-8C12-482E-B33D-AE59C37662CF">PSS_THREAD_ENTRY</a> structure, with basic information about the thread, as well as its termination state, suspend count and Win32 start address.


## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

