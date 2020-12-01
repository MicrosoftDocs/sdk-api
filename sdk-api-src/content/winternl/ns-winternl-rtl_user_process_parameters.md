---
UID: NS:winternl._RTL_USER_PROCESS_PARAMETERS
title: RTL_USER_PROCESS_PARAMETERS (winternl.h)
description: Contains process parameter information.
helpviewer_keywords: ["*PRTL_USER_PROCESS_PARAMETERS","PRTL_USER_PROCESS_PARAMETERS","PRTL_USER_PROCESS_PARAMETERS structure pointer","RTL_USER_PROCESS_PARAMETERS","RTL_USER_PROCESS_PARAMETERS structure","base.rtl_user_process_parameters","winternl/PRTL_USER_PROCESS_PARAMETERS","winternl/RTL_USER_PROCESS_PARAMETERS"]
old-location: base\rtl_user_process_parameters.htm
tech.root: backup
ms.assetid: e736aefa-9945-4526-84d8-adb6e82b9991
ms.date: 12/05/2018
ms.keywords: '*PRTL_USER_PROCESS_PARAMETERS, PRTL_USER_PROCESS_PARAMETERS, PRTL_USER_PROCESS_PARAMETERS structure pointer, RTL_USER_PROCESS_PARAMETERS, RTL_USER_PROCESS_PARAMETERS structure, base.rtl_user_process_parameters, winternl/PRTL_USER_PROCESS_PARAMETERS, winternl/RTL_USER_PROCESS_PARAMETERS'
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
req.typenames: RTL_USER_PROCESS_PARAMETERS, *PRTL_USER_PROCESS_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RTL_USER_PROCESS_PARAMETERS
 - winternl/_RTL_USER_PROCESS_PARAMETERS
 - PRTL_USER_PROCESS_PARAMETERS
 - winternl/PRTL_USER_PROCESS_PARAMETERS
 - RTL_USER_PROCESS_PARAMETERS
 - winternl/RTL_USER_PROCESS_PARAMETERS
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
 - RTL_USER_PROCESS_PARAMETERS
---

# RTL_USER_PROCESS_PARAMETERS structure


## -description

<p class="CCE_Message">[This structure may be altered in future versions of Windows.]

Contains process parameter information.

## -struct-fields

### -field Reserved1

Reserved for internal use by the operating system.

### -field Reserved2

Reserved for internal use by the operating system.

### -field ImagePathName

The path of the image file for the process.

### -field CommandLine

The command-line string passed to the process.

## -see-also

<a href="/windows/desktop/api/winternl/ns-winternl-peb">PEB</a>