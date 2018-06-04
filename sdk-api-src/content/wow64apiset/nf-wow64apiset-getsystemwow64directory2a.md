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

# GetSystemWow64Directory2A function


## -description


Retrieves the path of the system directory used by <a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a>, using the specified image file machine type. This directory is not present on 32-bit Windows.


## -parameters




### -param lpBuffer [out]

A pointer to the buffer to receive the path. This path does not end with a backslash.


### -param uSize [in]

The maximum size of the buffer, in <b>TCHARs</b>.


### -param ImageFileMachineType [in]

An <a href="https://msdn.microsoft.com/1E5E4F98-925B-424D-9B3D-BC6716FBF990">IMAGE_FILE_MACHINE_*</a> value that specifies the machine to test.


## -returns



If the function succeeds, the return value is the length, in <b>TCHARs</b>, of the string copied to the buffer, not including the terminating null character. If the length is greater than the size of the buffer, the return value is the size of the buffer required to hold the path.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



On systems that support multiple <a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">WOW64</a> architectures, you can use <b>GetSystemWow64Directory2</b> to retrieve appropriate system directory associated with the WOW64 architecture specified by <i>ImageFileMachineType</i>. 

WOW64 uses the system directory to store shared 32-bit code on 64-bit Windows. Most applications have no need to access this directory explicitly.

For more information on WOW64, see 
<a href="https://msdn.microsoft.com/ac75c5af-86e8-4282-9a8e-8db3c22cbda0">Running 32-bit Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/31ccd1bf-87c7-4df6-ae9d-5a3dfbd8b38b">GetSystemWow64Directory</a>
 

 

