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

# GetFileVersionInfoSizeA function


## -description


Determines whether the operating system can retrieve version information for a specified file. If version information is available, <b>GetFileVersionInfoSize</b> returns the size, in bytes, of that information. 


## -parameters




### -param lptstrFilename [in]

Type: <b>LPCTSTR</b>

The name of the file of interest. The function uses the search sequence specified by the  <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> function.
				


### -param lpdwHandle [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable that the function sets to zero.


## -returns



Type: <b>DWORD</b>

If the function succeeds, the return value is the size, in bytes, of the file's version information.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



Call the 
				<b>GetFileVersionInfoSize</b> function before calling the <a href="https://msdn.microsoft.com/44679c26-f1ac-409c-8a25-abc5bfd888ac">GetFileVersionInfo</a> function. The size returned by <b>GetFileVersionInfoSize</b> indicates the buffer size required for the version information returned by <b>GetFileVersionInfo</b>. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/44679c26-f1ac-409c-8a25-abc5bfd888ac">GetFileVersionInfo</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/7864510f-1894-4f17-bf7b-fd5bc1ba4aae">VS_VERSIONINFO</a>



<a href="https://msdn.microsoft.com/4fc3e2f0-0d9b-4974-b091-98908691bb14">VerQueryValue</a>



<a href="https://msdn.microsoft.com/60de7900-56b9-4481-bef9-b4079eedf926">Version Information</a>
 

 

