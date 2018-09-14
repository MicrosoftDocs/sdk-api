---
UID: NF:processsnapshot.PssWalkMarkerFree
title: PssWalkMarkerFree function
author: windows-sdk-content
description: Frees a walk marker created by PssWalkMarkerCreate.
old-location: proc_snap\psswalkmarkerfree.htm
tech.root: proc_snap
ms.assetid: 74158846-6A5F-4F81-B4D7-46DED1EE017C
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PssWalkMarkerFree, PssWalkMarkerFree function, proc_snap.psswalkmarkerfree, processsnapshot/PssWalkMarkerFree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - kernel32.dll
 - API-MS-Win-Core-Processsnapshot-l1-1-0.dll
 - KernelBase.dll
api_name:
 - PssWalkMarkerFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PssWalkMarkerFree function


## -description


Frees a walk marker created by <a href="https://msdn.microsoft.com/58E2FBAF-661C-45BE-A25A-A096AF52ED3E">PssWalkMarkerCreate</a>.


## -parameters




### -param WalkMarkerHandle [in]

A handle to the walk marker.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.




## -remarks



If <a href="https://msdn.microsoft.com/58E2FBAF-661C-45BE-A25A-A096AF52ED3E">PssWalkMarkerCreate</a> used <b>AllocRoutine</b> of a custom allocator to create the walk marker, <b>PssWalkMarkerFree</b> uses the <b>FreeRoutine</b> of the allocator.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

