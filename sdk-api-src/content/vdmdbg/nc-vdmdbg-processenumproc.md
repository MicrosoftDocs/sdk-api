---
UID: NC:vdmdbg.PROCESSENUMPROC
title: PROCESSENUMPROC (vdmdbg.h)
author: windows-sdk-content
description: Implement this function to receive information for each virtual DOS machine (VDM) that VDMEnumProcessWOW enumerates.
old-location: winprog\processvdms.htm
tech.root: DevNotes
ms.assetid: ba5ce19d-4f37-4764-9a76-0f1013f9ea0f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PROCESSENUMPROC, PROCESSENUMPROC callback, PROCESSENUMPROC callback function [Windows API], vdmdbg/PROCESSENUMPROC, winprog.processvdms
ms.topic: callback
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - VdmDbg.h
api_name:
 - PROCESSENUMPROC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PROCESSENUMPROC callback function


## -description


<p class="CCE_Message">[This function is not supported and may be altered or unavailable in the future.]

Implement this function to receive information for each virtual DOS machine (VDM) that <a href="https://msdn.microsoft.com/fd79ff50-cac2-40e0-86ad-2d6af97c99a9">VDMEnumProcessWOW</a> enumerates. 
			

The <b>PROCESSENUMPROC</b> type defines a pointer to this callback function. <b>ProcessVDMs</b> is a placeholder for the application-defined function name.


## -parameters




### -param dwProcessId [out]

The process ID of the NTVDM.exe process. Use this ID when calling other VDM debug functions.


### -param dwAttributes [out]

The process attributes.


### -param lpUserDefined [out]

The user-defined data that was passed to the <a href="https://msdn.microsoft.com/fd79ff50-cac2-40e0-86ad-2d6af97c99a9">VDMEnumProcessWOW</a> function.


## -returns



Return <b>TRUE</b> to stop the enumeration and <b>FALSE</b> to continue.



