---
UID: NF:processsnapshot.PssWalkMarkerSeekToBeginning
title: PssWalkMarkerSeekToBeginning function
author: windows-sdk-content
description: Rewinds a walk marker back to the beginning.
old-location: proc_snap\psswalkmarkerseektobeginning.htm
tech.root: proc_snap
ms.assetid: BE0FA122-3966-4827-9DA3-A98A162EF270
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PssWalkMarkerSeekToBeginning, PssWalkMarkerSeekToBeginning function, proc_snap.psswalkmarkerseektobeginning, processsnapshot/PssWalkMarkerSeekToBeginning
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
 - PssWalkMarkerSeekToBeginning
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PssWalkMarkerSeekToBeginning function


## -description


Rewinds a walk marker back to the beginning.


## -parameters




### -param WalkMarkerHandle [in]

A handle to the walk marker.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

