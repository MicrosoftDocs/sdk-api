---
UID: NF:loadperf.LoadPerfCounterTextStringsA
title: LoadPerfCounterTextStringsA function (loadperf.h)
description: Loads onto the computer the performance objects and counters defined in the specified initialization file.helpviewer_keywords: ["LoadPerfCounterTextStrings","LoadPerfCounterTextStrings function [Perf]","LoadPerfCounterTextStringsA","LoadPerfCounterTextStringsW","_win32_loadperfcountertextstrings","base.loadperfcountertextstrings","loadperf/LoadPerfCounterTextStrings","loadperf/LoadPerfCounterTextStringsA","loadperf/LoadPerfCounterTextStringsW","perf.loadperfcountertextstrings"]
old-location: perf\loadperfcountertextstrings.htm
tech.root: perfctrs
ms.assetid: 19f6989a-708a-485d-94c0-ab617707ced4
ms.date: 12/05/2018
ms.keywords: LoadPerfCounterTextStrings, LoadPerfCounterTextStrings function [Perf], LoadPerfCounterTextStringsA, LoadPerfCounterTextStringsW, _win32_loadperfcountertextstrings, base.loadperfcountertextstrings, loadperf/LoadPerfCounterTextStrings, loadperf/LoadPerfCounterTextStringsA, loadperf/LoadPerfCounterTextStringsW, perf.loadperfcountertextstrings
f1_keywords:
- loadperf/LoadPerfCounterTextStrings
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LoadPerfCounterTextStringsA function


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
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>.




## -remarks



This function provides an API to the functionality provided by the <b>Lodctr</b> tool. For information on <b>Lodctr</b>, see <a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/adding-counter-names-and-descriptions-to-the-registry">Adding Counter Names and Descriptions to the Registry</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/loadperf/nf-loadperf-unloadperfcountertextstringsa">UnloadPerfCounterTextStrings</a>
 

 

