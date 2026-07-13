---
UID: NS:winbase._STARTUPINFOEXA
title: STARTUPINFOEXA (winbase.h)
description: Specifies the window station, desktop, standard handles, and attributes for a new process. It is used with the CreateProcess and CreateProcessAsUser functions. (ANSI)
helpviewer_keywords: ["*LPSTARTUPINFOEXA","LPSTARTUPINFOEX","LPSTARTUPINFOEX structure pointer","STARTUPINFOEX","STARTUPINFOEX structure","STARTUPINFOEXA","STARTUPINFOEXW","_STARTUPINFOEXA","_STARTUPINFOEXW","base.startupinfoex","winbase/LPSTARTUPINFOEX","winbase/STARTUPINFOEX","winbase/STARTUPINFOEXA","winbase/STARTUPINFOEXW"]
old-location: base\startupinfoex.htm
tech.root: backup
ms.assetid: 61203f57-292d-4ea1-88f4-a3b05012d7a3
ms.date: 12/05/2018
ms.keywords: '*LPSTARTUPINFOEXA, LPSTARTUPINFOEX, LPSTARTUPINFOEX structure pointer, STARTUPINFOEX, STARTUPINFOEX structure, STARTUPINFOEXA, STARTUPINFOEXW, _STARTUPINFOEXA, _STARTUPINFOEXW, base.startupinfoex, winbase/LPSTARTUPINFOEX, winbase/STARTUPINFOEX, winbase/STARTUPINFOEXA, winbase/STARTUPINFOEXW'
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
targetos: Windows
req.typenames: STARTUPINFOEXA, *LPSTARTUPINFOEXA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _STARTUPINFOEXA
 - winbase/_STARTUPINFOEXA
 - LPSTARTUPINFOEXA
 - winbase/LPSTARTUPINFOEXA
 - STARTUPINFOEXA
 - winbase/STARTUPINFOEXA
dev_langs:
 - c++
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
---

# STARTUPINFOEXA structure


## -description

Specifies the window station, desktop, standard handles, and attributes for a new process. It is used with the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> and 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a> functions.

## -struct-fields

### -field StartupInfo

A <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure.

### -field lpAttributeList

An attribute list. This list is created by the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist">InitializeProcThreadAttributeList</a> function.

## -remarks

Be sure to set the <b>cb</b> member of the <a href="/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa">STARTUPINFO</a> structure to <code>sizeof(STARTUPINFOEX)</code>.





> [!NOTE]
> The winbase.h header defines STARTUPINFOEX as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera">CreateProcessAsUser</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-initializeprocthreadattributelist">InitializeProcThreadAttributeList</a>
