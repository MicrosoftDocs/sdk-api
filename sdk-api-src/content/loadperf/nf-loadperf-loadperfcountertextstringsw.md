---
UID: NF:loadperf.LoadPerfCounterTextStringsW
title: LoadPerfCounterTextStringsW function (loadperf.h)
description: Loads onto the computer the performance objects and counters defined in the specified initialization file. (Unicode)
helpviewer_keywords: ["LoadPerfCounterTextStrings", "LoadPerfCounterTextStrings function [Perf]", "LoadPerfCounterTextStringsW", "_win32_loadperfcountertextstrings", "base.loadperfcountertextstrings", "loadperf/LoadPerfCounterTextStrings", "loadperf/LoadPerfCounterTextStringsW", "perf.loadperfcountertextstrings"]
old-location: perf\loadperfcountertextstrings.htm
tech.root: perf
ms.assetid: 19f6989a-708a-485d-94c0-ab617707ced4
ms.date: 12/05/2018
ms.keywords: LoadPerfCounterTextStrings, LoadPerfCounterTextStrings function [Perf], LoadPerfCounterTextStringsA, LoadPerfCounterTextStringsW, _win32_loadperfcountertextstrings, base.loadperfcountertextstrings, loadperf/LoadPerfCounterTextStrings, loadperf/LoadPerfCounterTextStringsA, loadperf/LoadPerfCounterTextStringsW, perf.loadperfcountertextstrings
req.header: loadperf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: LoadPerfCounterTextStringsW (Unicode) and LoadPerfCounterTextStringsA (ANSI)
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
 - LoadPerfCounterTextStringsW
 - loadperf/LoadPerfCounterTextStringsW
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
 - LoadPerfCounterTextStrings
 - LoadPerfCounterTextStringsA
 - LoadPerfCounterTextStringsW
---

# LoadPerfCounterTextStringsW function


## -description

Loads onto the computer the performance objects and counters defined in the specified initialization file.

## -parameters

### -param lpCommandLine [in]

Null-terminated string that consists of one or more arbitrary letters, a space, and then the name of the initialization (.ini) file. The name can include the path to the initialization file. 

The function uses only the initialization file; the first argument is discarded. For example, to load an initialization file called "myfile.ini", the <i>commandLine</i> string could be "xx myfile.ini". The letters before the space (here "xx")  are discarded, and the second part, following the space, is interpreted as the initialization file specification.

### -param bQuietModeArg [in]

Set to <b>TRUE</b> to prevent the function from displaying the output from the  <b>Lodctr</b> tool; otherwise, <b>FALSE</b>. This parameter has meaning only if the application is run from a command prompt.

## -returns

If the function succeeds, it returns ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="/windows/desktop/Debug/system-error-codes">system error codes</a>.

## -remarks

This function provides an API to the functionality provided by the <b>Lodctr</b> tool. For information on <b>Lodctr</b>, see <a href="/windows/desktop/PerfCtrs/adding-counter-names-and-descriptions-to-the-registry">Adding Counter Names and Descriptions to the Registry</a>.





> [!NOTE]
> The loadperf.h header defines LoadPerfCounterTextStrings as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/loadperf/nf-loadperf-unloadperfcountertextstringsa">UnloadPerfCounterTextStrings</a>
