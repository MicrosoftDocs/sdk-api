---
UID: NF:loadperf.UnloadPerfCounterTextStringsA
title: UnloadPerfCounterTextStringsA function
author: windows-driver-content
description: Unloads performance objects and counters from the computer for the specified application.
old-location: perf\unloadperfcountertextstrings.htm
old-project: PerfCtrs
ms.assetid: f78858ca-d8d0-4178-9f9a-731b89cf5a61
ms.author: windowsdriverdev
ms.date: 3/22/2018
ms.keywords: UnloadPerfCounterTextStrings, UnloadPerfCounterTextStrings function [Perf], UnloadPerfCounterTextStringsA, UnloadPerfCounterTextStringsW, _win32_unloadperfcountertextstrings, base.unloadperfcountertextstrings, loadperf/UnloadPerfCounterTextStrings, loadperf/UnloadPerfCounterTextStringsA, loadperf/UnloadPerfCounterTextStringsW, perf.unloadperfcountertextstrings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: WKSTA_USER_INFO_1101, *PWKSTA_USER_INFO_1101, *LPWKSTA_USER_INFO_1101
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Loadperf.dll
api_name:
-	UnloadPerfCounterTextStrings
-	UnloadPerfCounterTextStringsA
-	UnloadPerfCounterTextStringsW
product: Windows
targetos: Windows
req.lib: Loadperf.lib
req.dll: Loadperf.dll
req.irql: 
req.product: GDI+ 1.1
---

# UnloadPerfCounterTextStringsA function


## -description


Unloads performance objects and counters from the computer for the specified application.
		


## -parameters




### -param lpCommandLine

TBD


### -param bQuietModeArg [in]

Set to <b>TRUE</b> to prevent the function from displaying the output from the  <b>Unlodctr</b> tool; otherwise, <b>FALSE</b>. This parameter has meaning only if the application is run from a command prompt.


#### - commandLine [in]

Null-terminated string that consists of one or more arbitrary letters, a space, and then the name of the application. The name of the application must match the <b>drivername</b> key value found in the initialization (.ini) file used to <a href="https://msdn.microsoft.com/19f6989a-708a-485d-94c0-ab617707ced4">load the text strings</a>.


## -returns




						If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.




## -remarks



This function provides an API to the functionality provided by <b>Unlodctr</b> tool. For more information, see <a href="https://msdn.microsoft.com/83c0fb91-857c-40d9-8fb8-8734c1b573c4">Removing Counter Names and Descriptions from the Registry</a>.




## -see-also




<a href="https://msdn.microsoft.com/19f6989a-708a-485d-94c0-ab617707ced4">LoadPerfCounterTextStrings</a>
 

 

