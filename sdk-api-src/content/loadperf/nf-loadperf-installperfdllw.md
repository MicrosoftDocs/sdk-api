---
UID: NF:loadperf.InstallPerfDllW
title: InstallPerfDllW function (loadperf.h)
description: Installs performance counter strings, as defined in an input .ini file, into the system registry. (Unicode)
helpviewer_keywords: ["InstallPerfDll", "InstallPerfDll function [Windows API]", "InstallPerfDllW", "loadperf/InstallPerfDll", "winprog.installperfdll"]
old-location: winprog\installperfdll.htm
tech.root: winprog
ms.assetid: d674f023-27e5-4ca2-926d-4fa02292ffbb
ms.date: 12/05/2018
ms.keywords: InstallPerfDll, InstallPerfDll function [Windows API], InstallPerfDllA, InstallPerfDllW, loadperf/InstallPerfDll, winprog.installperfdll
req.header: loadperf.h
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
req.dll: Loadperf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InstallPerfDllW
 - loadperf/InstallPerfDllW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Loadperf.dll
api_name:
 - InstallPerfDll
 - InstallPerfDllW
---

# InstallPerfDllW function


## -description

Installs performance counter strings, as defined in an input .ini file, into the system registry.
<div class="alert"><b>Note</b>  Microsoft recommends that developers use <a href="/windows/desktop/api/loadperf/nf-loadperf-loadperfcountertextstringsa">LoadPerfCounterTextStrings</a> instead of <b>InstallPerfDll</b>. <b>LoadPerfCounterTextStrings</b> calls <b>InstallPerfDll</b> internally. </div><div> </div>

## -parameters

### -param szComputerName [in]

The name of the system. This should be <b>NULL</b> because this function cannot be used to install remotely.

### -param lpIniFile [in]

The name of the initialization file that contains definitions to  add to the registry.

### -param dwFlags [in]

This parameter can be <b>LOADPERF_FLAGS_DISPLAY_USER_MSGS</b> (<code>(ULONG_PTR) 8</code>).

## -returns

If the function is successful, it returns <b>TRUE</b> and posts additional information in  an application event log. Otherwise, it returns an error code that represents the condition that caused the failure.

## -remarks

This function has no associated import library; you must call it using the <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> and <a href="/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> functions.





> [!NOTE]
> The loadperf.h header defines InstallPerfDll as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/loadperf/nf-loadperf-loadperfcountertextstringsa">LoadPerfCounterTextStrings</a>
