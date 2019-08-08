---
UID: NS:winbase._STARTUPINFOEXA
title: STARTUPINFOEXA (winbase.h)
author: windows-sdk-content
description: Specifies the window station, desktop, standard handles, and attributes for a new process. It is used with the CreateProcess and CreateProcessAsUser functions.
old-location: base\startupinfoex.htm
tech.root: ProcThread
ms.assetid: 61203f57-292d-4ea1-88f4-a3b05012d7a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: '*LPSTARTUPINFOEXA, LPSTARTUPINFOEX, LPSTARTUPINFOEX structure pointer, STARTUPINFOEX, STARTUPINFOEX structure, STARTUPINFOEXA, STARTUPINFOEXW, _STARTUPINFOEXA, _STARTUPINFOEXW, base.startupinfoex, winbase/LPSTARTUPINFOEX, winbase/STARTUPINFOEX, winbase/STARTUPINFOEXA, winbase/STARTUPINFOEXW'
ms.topic: struct
f1_keywords:
- winbase/STARTUPINFOEX
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: STARTUPINFOEXW (Unicode) and STARTUPINFOEXA (ANSI)
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
- WinBase.h
api_name:
- STARTUPINFOEX
- STARTUPINFOEXA
- STARTUPINFOEXW
product: Windows
targetos: Windows
req.typenames: STARTUPINFOEXA, *LPSTARTUPINFOEXA
req.redist: 
ms.custom: 19H1
---

# STARTUPINFOEXA structure


## -description


Specifies the window station, desktop, standard handles, and attributes for a new process. It is used with the 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> functions.


## -struct-fields




### -field StartupInfo

A <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure.


### -field lpAttributeList

An attribute list. This list is created by the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist">InitializeProcThreadAttributeList</a> function.


## -remarks



Be sure to set the <b>cb</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure to <code>sizeof(STARTUPINFOEX)</code>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="https://docs.microsoft.com/windows/desktop/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist">InitializeProcThreadAttributeList</a>
 

 

