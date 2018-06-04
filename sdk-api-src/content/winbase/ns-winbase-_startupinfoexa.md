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

# _STARTUPINFOEXA structure


## -description


Specifies the window station, desktop, standard handles, and attributes for a new process. It is used with the 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> and 
<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a> functions.


## -struct-fields




### -field StartupInfo

A <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure.


### -field lpAttributeList

An attribute list. This list is created by the <a href="https://msdn.microsoft.com/58ce70a1-5b73-429f-a062-bacd9b9c5bc8">InitializeProcThreadAttributeList</a> function.


## -remarks



Be sure to set the <b>cb</b> member of the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure to <code>sizeof(STARTUPINFOEX)</code>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>



<a href="https://msdn.microsoft.com/6b3f4dd9-500b-420e-804a-401a9e188be8">CreateProcessAsUser</a>



<a href="https://msdn.microsoft.com/58ce70a1-5b73-429f-a062-bacd9b9c5bc8">InitializeProcThreadAttributeList</a>
 

 

