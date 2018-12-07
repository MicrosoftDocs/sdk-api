---
UID: NE:processsnapshot.PSS_WALK_INFORMATION_CLASS
title: PSS_WALK_INFORMATION_CLASS
author: windows-sdk-content
description: Specifies what information the PssWalkSnapshot function returns.
old-location: proc_snap\pss_walk_information_class.htm
tech.root: proc_snap
ms.assetid: 93A79F7F-2164-4F7A-ADE7-C1655EEFC9BF
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: PSS_WALK_AUXILIARY_PAGES, PSS_WALK_HANDLES, PSS_WALK_INFORMATION_CLASS, PSS_WALK_INFORMATION_CLASS enumeration, PSS_WALK_THREADS, PSS_WALK_VA_SPACE, proc_snap.pss_walk_information_class, processsnapshot/PSS_WALK_AUXILIARY_PAGES, processsnapshot/PSS_WALK_HANDLES, processsnapshot/PSS_WALK_INFORMATION_CLASS, processsnapshot/PSS_WALK_THREADS, processsnapshot/PSS_WALK_VA_SPACE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: processsnapshot.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - processsnapshot.h
api_name:
 - PSS_WALK_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: PSS_WALK_INFORMATION_CLASS
req.redist: 
---

# PSS_WALK_INFORMATION_CLASS enumeration


## -description


Specifies what information the <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a> function returns.


## -enum-fields




### -field PSS_WALK_AUXILIARY_PAGES

Returns a <a href="https://msdn.microsoft.com/A3D948E6-6FFE-4732-A8C7-A292FDA07D7C">PSS_AUXILIARY_PAGE_ENTRY</a> structure, which contains the address, page attributes and contents of an auxiliary copied page.


### -field PSS_WALK_VA_SPACE

Returns a <a href="https://msdn.microsoft.com/69B8F6A3-76DF-421B-B89B-73BA3254F897">PSS_VA_SPACE_ENTRY</a> structure, which contains the <a href="https://msdn.microsoft.com/dc3fa48e-0986-49cc-88a9-ff8179fbe5f0">MEMORY_BASIC_INFORMATION</a> structure for every distinct VA region.


### -field PSS_WALK_HANDLES

Returns a <a href="https://msdn.microsoft.com/F56E8C35-949A-4DEE-973F-CF24F6596036">PSS_HANDLE_ENTRY</a> structure, with information specifying the handle value, its type name, object name (if captured), basic information (if captured), and type-specific information (if captured).


### -field PSS_WALK_THREADS

Returns a <a href="https://msdn.microsoft.com/99C89DBB-8C12-482E-B33D-AE59C37662CF">PSS_THREAD_ENTRY</a> structure, with basic information about the thread, as well as its termination state, suspend count and Win32 start address.


## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

