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

# InstallPerfDllA function


## -description


Installs performance counter strings, as defined in an input .ini file, into the system registry.
<div class="alert"><b>Note</b>  Microsoft recommends that developers use <a href="https://msdn.microsoft.com/19f6989a-708a-485d-94c0-ab617707ced4">LoadPerfCounterTextStrings</a> instead of <b>InstallPerfDll</b>. <b>LoadPerfCounterTextStrings</b> calls <b>InstallPerfDll</b> internally. </div><div> </div>

## -parameters




### -param szComputerName [in]

The name of the system. This should be <b>NULL</b> because this function cannot be used to install remotely.


### -param lpIniFile

TBD


### -param dwFlags [in]

This parameter can be <b>LOADPERF_FLAGS_DISPLAY_USER_MSGS</b> (<code>(ULONG_PTR) 8</code>).


#### - szIniFile [in]

The name of the initialization file that contains definitions to  add to the registry.


## -returns



If the function is successful, it returns <b>TRUE</b> and posts additional information in  an application event log. Otherwise, it returns an error code that represents the condition that caused the failure.




## -remarks



This function has no associated import library; you must call it using the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions.




## -see-also




<a href="https://msdn.microsoft.com/19f6989a-708a-485d-94c0-ab617707ced4">LoadPerfCounterTextStrings</a>
 

 

