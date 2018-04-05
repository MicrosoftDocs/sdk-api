---
UID: NS:processsnapshot.PSS_ALLOCATOR
title: PSS_ALLOCATOR
author: windows-driver-content
description: Specifies custom functions which the Process Snapshotting functions use to allocate and free the internal walk marker structures.
old-location: proc_snap\pss_allocator.htm
old-project: proc_snap
ms.assetid: 54225F76-9A2E-4CB3-A3B5-9F9DB5551D53
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: PSS_ALLOCATOR, PSS_ALLOCATOR structure, proc_snap.pss_allocator, processsnapshot/PSS_ALLOCATOR
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: PSS_ALLOCATOR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	processsnapshot.h
api_name:
-	PSS_ALLOCATOR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PSS_ALLOCATOR structure


## -description


Specifies custom functions which the Process Snapshotting functions use to allocate and free the internal walk marker structures.


## -struct-fields




### -field Context

An arbitrary pointer-sized value that the Process Snapshotting functions pass to <b>AllocRoutine</b> and <b>FreeRoutine</b>.


### -field AllocRoutine

A pointer to a WINAPI-calling convention function that takes two parameters. It returns a pointer to the block of memory that it allocates, or <b>NULL</b> if allocation fails.



#### Context

The context value, as passed in <b>PSS_ALLOCATOR</b>.



#### Size

Number of bytes to allocate.


### -field FreeRoutine

A pointer to a WINAPI-calling convention function taking two parameters. It deallocates a block of memory that <b>AllocRoutine</b> allocated.



#### Context

The context value, as passed in <b>PSS_ALLOCATOR</b>.



#### Address

The address of a block of memory that <b>AllocRoutine</b> allocated.


## -remarks



To use custom memory allocation functions, pass this structure to <a href="https://msdn.microsoft.com/58E2FBAF-661C-45BE-A25A-A096AF52ED3E">PssWalkMarkerCreate</a>. Otherwise, the Process Snapshotting functions use  the default process heap.

The <b>PSS_ALLOCATOR</b> structure that provides the custom functions should remain valid for the lifetime of the walk marker that <a href="https://msdn.microsoft.com/58E2FBAF-661C-45BE-A25A-A096AF52ED3E">PssWalkMarkerCreate</a> creates. 

<b>FreeRoutine</b> must accept <b>NULL</b> address parameters without failing.

The custom functions are called from <a href="https://msdn.microsoft.com/58E2FBAF-661C-45BE-A25A-A096AF52ED3E">PssWalkMarkerCreate</a>, <a href="https://msdn.microsoft.com/74158846-6A5F-4F81-B4D7-46DED1EE017C">PssWalkMarkerFree</a> and <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a> using the same thread that calls <b>PssWalkMarkerCreate</b>, <b>PssWalkMarkerFree</b> and <b>PssWalkSnapshot</b>. Therefore the custom functions need not be multi-threaded.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

