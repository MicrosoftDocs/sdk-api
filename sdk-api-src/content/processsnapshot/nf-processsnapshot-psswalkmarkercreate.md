---
UID: NF:processsnapshot.PssWalkMarkerCreate
title: PssWalkMarkerCreate function
author: windows-sdk-content
description: Creates a walk marker.
old-location: proc_snap\psswalkmarkercreate.htm
old-project: proc_snap
ms.assetid: 58E2FBAF-661C-45BE-A25A-A096AF52ED3E
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: PssWalkMarkerCreate, PssWalkMarkerCreate function, proc_snap.psswalkmarkercreate, processsnapshot/PssWalkMarkerCreate
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
 - PssWalkMarkerCreate
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# PssWalkMarkerCreate function


## -description


Creates a walk marker.


## -parameters




### -param Allocator [in, optional]

A structure that provides functions to allocate and free memory.  If you provide the structure, <b>PssWalkMarkerCreate</b> uses the functions to  allocate the internal walk marker structures. Otherwise it uses the default process heap. For more information, see <a href="https://msdn.microsoft.com/54225F76-9A2E-4CB3-A3B5-9F9DB5551D53">PSS_ALLOCATOR</a>.


### -param WalkMarkerHandle [out]

A handle to the walk marker that this function creates.


## -returns



This function returns <b>ERROR_SUCCESS</b> on success or the following error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Could not allocate memory for the walk marker.

</td>
</tr>
</table>
 

All error codes are defined in winerror.h. Use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> with the <b>FORMAT_MESSAGE_FROM_SYSTEM</b> flag to get a message for an error code.




## -remarks



The walk marker maintains the state of a walk, and can be used to reposition or rewind the walk.

The <i>Allocator</i> structure that provides the custom functions should remain valid for the lifetime of the walk marker. The custom functions are called from <b>PssWalkMarkerCreate</b>, <a href="https://msdn.microsoft.com/74158846-6A5F-4F81-B4D7-46DED1EE017C">PssWalkMarkerFree</a> and <a href="https://msdn.microsoft.com/C6AC38B5-0A1C-44D7-A1F6-8196AE9B8FB0">PssWalkSnapshot</a> using the same thread that calls <b>PssWalkMarkerCreate</b>, <b>PssWalkMarkerFree</b> and <b>PssWalkSnapshot</b>. Therefore the custom functions need not be multi-threaded.




## -see-also




<a href="https://msdn.microsoft.com/1dc6fe86-3f5a-4810-8e93-a0fe309c54ee">Process Snapshotting</a>
 

 

