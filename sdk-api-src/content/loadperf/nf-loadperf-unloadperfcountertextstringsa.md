---
UID: NF:loadperf.UnloadPerfCounterTextStringsA
title: UnloadPerfCounterTextStringsA function (loadperf.h)
description: Unloads performance objects and counters from the computer for the specified application. (ANSI)
helpviewer_keywords: ["UnloadPerfCounterTextStringsA", "loadperf/UnloadPerfCounterTextStringsA"]
old-location: perf\unloadperfcountertextstrings.htm
tech.root: perf
ms.assetid: f78858ca-d8d0-4178-9f9a-731b89cf5a61
ms.date: 12/05/2018
ms.keywords: UnloadPerfCounterTextStrings, UnloadPerfCounterTextStrings function [Perf], UnloadPerfCounterTextStringsA, UnloadPerfCounterTextStringsW, _win32_unloadperfcountertextstrings, base.unloadperfcountertextstrings, loadperf/UnloadPerfCounterTextStrings, loadperf/UnloadPerfCounterTextStringsA, loadperf/UnloadPerfCounterTextStringsW, perf.unloadperfcountertextstrings
req.header: loadperf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UnloadPerfCounterTextStringsW (Unicode) and UnloadPerfCounterTextStringsA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Loadperf.lib
req.dll: Loadperf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UnloadPerfCounterTextStringsA
 - loadperf/UnloadPerfCounterTextStringsA
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
 - UnloadPerfCounterTextStrings
 - UnloadPerfCounterTextStringsA
 - UnloadPerfCounterTextStringsW
---

# UnloadPerfCounterTextStringsA function


## -description

Unloads performance objects and counters from the computer for the specified application.

## -parameters

### -param lpCommandLine [in]

Null-terminated string that consists of one or more arbitrary letters, a space, and then the name of the application. The name of the application must match the <b>drivername</b> key value found in the initialization (.ini) file used to <a href="/windows/desktop/api/loadperf/nf-loadperf-loadperfcountertextstringsa">load the text strings</a>.

### -param bQuietModeArg [in]

Set to <b>TRUE</b> to prevent the function from displaying the output from the <b>Unlodctr</b> tool; otherwise, <b>FALSE</b>. This parameter has meaning only if the application is run from a command prompt.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

This function provides an API to the functionality provided by <b>Unlodctr</b> tool. For more information, see <a href="/windows/desktop/PerfCtrs/removing-counter-names-and-descriptions-from-the-registry">Removing Counter Names and Descriptions from the Registry</a>.





> [!NOTE]
> The loadperf.h header defines UnloadPerfCounterTextStrings as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/loadperf/nf-loadperf-loadperfcountertextstringsa">LoadPerfCounterTextStrings</a>
