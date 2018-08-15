---
UID: NF:loadperf.LoadPerfCounterTextStringsA
title: LoadPerfCounterTextStringsA function
author: windows-sdk-content
description: Loads onto the computer the performance objects and counters defined in the specified initialization file.
old-location: perf\loadperfcountertextstrings.htm
old-project: PerfCtrs
ms.assetid: 19f6989a-708a-485d-94c0-ab617707ced4
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: LoadPerfCounterTextStrings, LoadPerfCounterTextStrings function [Perf], LoadPerfCounterTextStringsA, LoadPerfCounterTextStringsW, _win32_loadperfcountertextstrings, base.loadperfcountertextstrings, loadperf/LoadPerfCounterTextStrings, loadperf/LoadPerfCounterTextStringsA, loadperf/LoadPerfCounterTextStringsW, perf.loadperfcountertextstrings
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: loadperf.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, *LPWKSTA_USER_INFO_1101
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
product: Windows
targetos: Windows
req.lib: Loadperf.lib
req.dll: Loadperf.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



This function provides an API to the functionality provided by the <b>Lodctr</b> tool. For information on <b>Lodctr</b>, see <a href="https://msdn.microsoft.com/6fdaccb0-45bc-48f2-8f63-3df0bdf1dca4">Adding Counter Names and Descriptions to the Registry</a>.




## -see-also




<a href="https://msdn.microsoft.com/f78858ca-d8d0-4178-9f9a-731b89cf5a61">UnloadPerfCounterTextStrings</a>
 

 

