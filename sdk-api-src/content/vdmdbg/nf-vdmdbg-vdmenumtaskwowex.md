---
UID: NF:vdmdbg.VDMEnumTaskWOWEx
title: VDMEnumTaskWOWEx function
author: windows-sdk-content
description: Enumerates tasks within a particular virtual DOS machine (VDM).
old-location: winprog\vdmenumtaskwowex.htm
tech.root: devnotes
ms.assetid: c09c5d80-9de6-424b-bd57-bf6a450221e4
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: VDMEnumTaskWOWEx, VDMEnumTaskWOWEx function [Windows API], vdmdbg/VDMEnumTaskWOWEx, winprog.vdmenumtaskwowex
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vdmdbg.h
req.include-header: 
req.target-type: Windows
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
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VdmDbg.dll
api_name:
 - VDMEnumTaskWOWEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VDMEnumTaskWOWEx function


## -description


<p class="CCE_Message">[This function is not supported and may be altered or unavailable in the future.]

Enumerates tasks within a particular virtual DOS machine (VDM).


## -parameters




### -param dwProcessId [in]

The process identifier of the VDM. This should be the process identifier that the <b>VDMEnumProcessWOW</b> function returns.


### -param fp [in]

A pointer to a callback function. The function is called for each enumerated task. For details, see the <a href="https://msdn.microsoft.com/0ef6b3b0-1b65-4919-8857-33651b9c154f">ProcessTask</a> callback function.


### -param lparam [in]

A user-defined value that is passed to the callback function.


## -returns



The number of tasks running within the specified VDM, or the number enumerated before enumeration was terminated.




## -remarks



VdmDbg.dll contains many functions that are useful for working with 16-bit applications. For more details on using some of the VDM debug functions, see knowledge base article KB182559.


#### Examples

For an example, see <a href="https://msdn.microsoft.com/fd79ff50-cac2-40e0-86ad-2d6af97c99a9">VDMEnumProcessWOW</a>.

<div class="code"></div>


