---
UID: NF:processsnapshot.PssWalkMarkerGetPosition
title: PssWalkMarkerGetPosition function
author: windows-sdk-content
description: Returns the current position of a walk marker.
old-location: proc_snap\psswalkmarkergetposition.htm
old-project: proc_snap
ms.assetid: A2058E81-2B01-4436-ACC6-2A3E58BC4E27
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: PssWalkMarkerGetPosition, PssWalkMarkerGetPosition function, proc_snap.psswalkmarkergetposition, processsnapshot/PssWalkMarkerGetPosition
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: PSS_WALK_INFORMATION_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	kernel32.dll
-	API-MS-Win-Core-Processsnapshot-l1-1-0.dll
-	KernelBase.dll
api_name:
-	PssWalkMarkerGetPosition
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PssWalkMarkerGetPosition function


## -description


Returns the current position of a walk marker.


## -parameters




### -param WalkMarkerHandle [in]

A  handle to the walk marker.


### -param Position [out]

The walk marker position that this function returns.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success.

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.




## -remarks



The position value compared to the values of other positions is not of any significance. The only valid use of the position is to set the current position using the <a href="https://msdn.microsoft.com/D89EA4DB-D8C6-43D1-B292-D24F1EAB2E43">PssWalkMarkerSetPosition</a> function.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

