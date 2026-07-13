---
UID: NF:setupapi.SetupIterateCabinetA
title: SetupIterateCabinetA function (setupapi.h)
description: The SetupIterateCabinet function iterates through all the files in a cabinet and sends a notification to a callback function for each file found. (ANSI)
helpviewer_keywords: ["SetupIterateCabinetA", "setupapi/SetupIterateCabinetA"]
old-location: setup\setupiteratecabinet.htm
tech.root: setup
ms.assetid: 2fa2d140-fa8e-41a8-9800-d10e5559fab4
ms.date: 12/05/2018
ms.keywords: SetupIterateCabinet, SetupIterateCabinet function [Setup API], SetupIterateCabinetA, SetupIterateCabinetW, _setupapi_setupiteratecabinet, setup.setupiteratecabinet, setupapi/SetupIterateCabinet, setupapi/SetupIterateCabinetA, setupapi/SetupIterateCabinetW
req.header: setupapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetupIterateCabinetW (Unicode) and SetupIterateCabinetA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Setupapi.lib
req.dll: Setupapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetupIterateCabinetA
 - setupapi/SetupIterateCabinetA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Setupapi.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-1.dll
 - Ext-MS-Win-SetupAPI-ClassInstallers-L1-1-2.dll
api_name:
 - SetupIterateCabinet
 - SetupIterateCabinetA
 - SetupIterateCabinetW
req.apiset: ext-ms-win-setupapi-classinstallers-l1-1-2 (introduced in Windows 10, version 10.0.14393)
---

# SetupIterateCabinetA function


## -description

<p class="CCE_Message">[This function is available for use in the operating systems indicated in the Requirements section. It may be altered or unavailable in subsequent versions.   SetupAPI should no longer be used for installing applications. Instead, use the Windows Installer for developing application installers. SetupAPI continues to be used for installing device drivers.]

The 
<b>SetupIterateCabinet</b> function iterates through all the files in a cabinet and sends a notification to a callback function for each file found.

## -parameters

### -param CabinetFile [in]

Cabinet (.CAB) file to iterate through.

### -param Reserved [in]

Not currently used.

### -param MsgHandler [in]

Pointer to a <a href="/windows/desktop/api/setupapi/nc-setupapi-psp_file_callback_a">FileCallback</a> routine that will process the notifications 
<b>SetupIterateCabinet</b> returns as it iterates through the files in the cabinet file. The callback routine may then return a value specifying whether to decompress, copy, or skip the file.

### -param Context [in]

Context value that is passed into the routine specified in <i>MsgHandler</i>. This enables the callback routine to track values between notifications, without having to use global variables.

## -returns

If the function succeeds, the return value is a nonzero value.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SetupApi/functions">Functions</a>



<a href="/windows/desktop/SetupApi/overview">Overview</a>

## -remarks

> [!NOTE]
> The setupapi.h header defines SetupIterateCabinet as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
