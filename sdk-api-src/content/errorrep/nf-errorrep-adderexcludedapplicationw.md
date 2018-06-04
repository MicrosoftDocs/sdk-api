---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# AddERExcludedApplicationW function


## -description


<p class="CCE_Message">[The AddERExcludedApplication function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use the <a href="https://msdn.microsoft.com/ac1ec373-868f-4634-8658-4253d4f5923a">WerAddExcludedApplication</a> function.]

Excludes the specified application from error reporting.


## -parameters




### -param wszApplication

TBD




#### - szApplication [in]

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
 

 

