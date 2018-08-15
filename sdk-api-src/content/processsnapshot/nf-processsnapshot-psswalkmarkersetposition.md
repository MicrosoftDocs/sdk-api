---
UID: NF:processsnapshot.PssWalkMarkerSetPosition
title: PssWalkMarkerSetPosition function
author: windows-sdk-content
description: Sets the position of a walk marker.
old-location: proc_snap\psswalkmarkersetposition.htm
old-project: proc_snap
ms.assetid: D89EA4DB-D8C6-43D1-B292-D24F1EAB2E43
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: PssWalkMarkerSetPosition, PssWalkMarkerSetPosition function, proc_snap.psswalkmarkersetposition, processsnapshot/PssWalkMarkerSetPosition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: processsnapshot.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PSS_WALK_INFORMATION_CLASS
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
 - PssWalkMarkerSetPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# PssWalkMarkerSetPosition function


## -description


Sets the position of a walk marker.


## -parameters




### -param WalkMarkerHandle [in]

A handle to the walk marker.


### -param Position [in]

The position to set. This is a position that the  <a href="https://msdn.microsoft.com/A2058E81-2B01-4436-ACC6-2A3E58BC4E27">PssWalkMarkerGetPosition</a> function provided.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success or one of the following error codes.

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

