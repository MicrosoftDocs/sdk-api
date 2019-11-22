---
UID: NF:loadperf.UnloadPerfCounterTextStringsW
title: UnloadPerfCounterTextStringsW function (loadperf.h)

description: Unloads performance objects and counters from the computer for the specified application.
old-location: perf\unloadperfcountertextstrings.htm
tech.root: perfctrs
ms.assetid: f78858ca-d8d0-4178-9f9a-731b89cf5a61

ms.date: 12/05/2018
ms.keywords: UnloadPerfCounterTextStrings, UnloadPerfCounterTextStrings function [Perf], UnloadPerfCounterTextStringsA, UnloadPerfCounterTextStringsW, _win32_unloadperfcountertextstrings, base.unloadperfcountertextstrings, loadperf/UnloadPerfCounterTextStrings, loadperf/UnloadPerfCounterTextStringsA, loadperf/UnloadPerfCounterTextStringsW, perf.unloadperfcountertextstrings
ms.topic: function
f1_keywords: 
 - "loadperf/UnloadPerfCounterTextStrings"
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
req.unicode-ansi: UnloadPerfCounterTextStringsW (Unicode) and UnloadPerfCounterTextStringsA (ANSI)
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
 - UnloadPerfCounterTextStrings
 - UnloadPerfCounterTextStringsA
 - UnloadPerfCounterTextStringsW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UnloadPerfCounterTextStringsW function


## -description


Unloads performance objects and counters from the computer for the specified application.
		


## -parameters




### -param lpCommandLine [in]

Null-terminated string that consists of one or more arbitrary letters, a space, and then the name of the application. The name of the application must match the <b>drivername</b> key value found in the initialization (.ini) file used to <a href="https://docs.microsoft.com/windows/desktop/api/loadperf/nf-loadperf-loadperfcountertextstringsa">load the text strings</a>.


### -param bQuietModeArg [in]

Set to <b>TRUE</b> to prevent the function from displaying the output from the  <b>Unlodctr</b> tool; otherwise, <b>FALSE</b>. This parameter has meaning only if the application is run from a command prompt.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>.




## -remarks



This function provides an API to the functionality provided by <b>Unlodctr</b> tool. For more information, see <a href="https://docs.microsoft.com/windows/desktop/PerfCtrs/removing-counter-names-and-descriptions-from-the-registry">Removing Counter Names and Descriptions from the Registry</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/loadperf/nf-loadperf-loadperfcountertextstringsa">LoadPerfCounterTextStrings</a>
 

 

