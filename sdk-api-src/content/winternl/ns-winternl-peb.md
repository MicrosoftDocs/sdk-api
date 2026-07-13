---
UID: NS:winternl._PEB
title: PEB (winternl.h)
description: Contains process information.
helpviewer_keywords: ["*PPEB","PEB","PEB structure","PPEB","PPEB structure pointer","base.peb","winternl/PEB","winternl/PPEB"]
old-location: base\peb.htm
tech.root: backup
ms.assetid: 836a6b82-d3e8-4de6-808d-5476dfb51356
ms.date: 12/05/2018
ms.keywords: '*PPEB, PEB, PEB structure, PPEB, PPEB structure pointer, base.peb, winternl/PEB, winternl/PPEB'
req.header: winternl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
targetos: Windows
req.typenames: PEB, *PPEB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PEB
 - winternl/_PEB
 - PPEB
 - winternl/PPEB
 - PEB
 - winternl/PEB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winternl.h
api_name:
 - PEB
---

# PEB structure


## -description

<p class="CCE_Message">[This structure may be altered in future versions of Windows.]

Contains process information.

## -struct-fields

### -field Reserved1

Reserved for internal use by the operating system.

### -field BeingDebugged

Indicates whether the specified process is currently being debugged. The <b>PEB</b> structure, however, is an internal operating-system structure whose layout may change in the future. It is best to use the <a href="/windows/desktop/api/debugapi/nf-debugapi-checkremotedebuggerpresent">CheckRemoteDebuggerPresent</a> function instead.

### -field Reserved2

Reserved for internal use by the operating system.

### -field Reserved3

Reserved for internal use by the operating system.

### -field Ldr

A pointer to a <a href="/windows/desktop/api/winternl/ns-winternl-peb_ldr_data">PEB_LDR_DATA</a> structure that contains information about the loaded modules for the process.

### -field ProcessParameters

A pointer to an <a href="/windows/desktop/api/winternl/ns-winternl-rtl_user_process_parameters">RTL_USER_PROCESS_PARAMETERS</a> structure that contains process parameter information such as the command line.

### -field Reserved4

Reserved for internal use by the operating system.

### -field AtlThunkSListPtr

### -field Reserved5

Reserved for internal use by the operating system.

### -field Reserved6

Reserved for internal use by the operating system.

### -field Reserved7

Reserved for internal use by the operating system.

### -field Reserved8

### -field AtlThunkSListPtr32

### -field Reserved9

### -field Reserved10

### -field PostProcessInitRoutine

Not supported.

### -field Reserved11

### -field Reserved12

### -field SessionId

The Terminal Services session identifier associated with the current process.

## -remarks

The syntax for this structure on 64-bit Windows is as follows:


``` syntax
typedef struct _PEB {
    BYTE Reserved1[2];
    BYTE BeingDebugged;
    BYTE Reserved2[21];
    PPEB_LDR_DATA LoaderData;
    PRTL_USER_PROCESS_PARAMETERS ProcessParameters;
    BYTE Reserved3[520];
    PPS_POST_PROCESS_INIT_ROUTINE PostProcessInitRoutine;
    BYTE Reserved4[136];
    ULONG SessionId;
} PEB;
```


## -see-also


<a href="/windows/desktop/api/winternl/nf-winternl-ntqueryinformationprocess">NtQueryInformationProcess</a>

<a href="/windows/desktop/ProcThread/zwqueryinformationprocess">ZwQueryInformationProcess</a>



<a href="/windows/win32/api/winternl/ns-winternl-teb">TEB</a>



<a href="/windows/desktop/api/winternl/ns-winternl-peb_ldr_data">PEB_LDR_DATA</a>



<a href="/windows/desktop/api/winternl/ns-winternl-rtl_user_process_parameters">RTL_USER_PROCESS_PARAMETERS</a>

