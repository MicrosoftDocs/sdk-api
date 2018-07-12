---
UID: NF:errorrep.AddERExcludedApplicationA
title: AddERExcludedApplicationA function
author: windows-sdk-content
description: Excludes the specified application from error reporting.
old-location: wer\adderexcludedapplication.htm
old-project: wer
ms.assetid: 9055437b-2ee2-4f0a-bcef-2b04ac5368b3
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: AddERExcludedApplication, AddERExcludedApplication function [Windows Error Reporting], AddERExcludedApplicationA, AddERExcludedApplicationW, _win32_adderexcludedapplication, base.adderexcludedapplication, errorrep/AddERExcludedApplication, errorrep/AddERExcludedApplicationA, errorrep/AddERExcludedApplicationW, wer.adderexcludedapplication
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: errorrep.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: AddERExcludedApplicationW (Unicode) and AddERExcludedApplicationA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AUDIO_VOLUME_NOTIFICATION_DATA, *PAUDIO_VOLUME_NOTIFICATION_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Faultrep.dll
api_name:
 - AddERExcludedApplication
 - AddERExcludedApplicationA
 - AddERExcludedApplicationW
product: Windows
targetos: Windows
req.lib: Faultrep.lib
req.dll: Faultrep.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# AddERExcludedApplicationA function


## -description


<p class="CCE_Message">[The AddERExcludedApplication function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/ac1ec373-868f-4634-8658-4253d4f5923a">WerAddExcludedApplication</a> function.]

Excludes the specified application from error reporting.


## -parameters




### -param szApplication [in]

The name of the executable file for the application, including the file name extension. The name cannot contain path information.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, see 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



This function stores the excluded application list under the <b>HKEY_LOCAL_MACHINE</b> hive. The calling process must have permissions to write to this registry hive.




## -see-also




<a href="https://msdn.microsoft.com/9f7c2abc-4d9a-4f3b-a540-e4546ed709de">ReportFault</a>



<a href="https://msdn.microsoft.com/4e28f379-5793-4d76-898e-d87a0291c034">WER Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/jj242491">Windows Error Reporting</a>
 

 

