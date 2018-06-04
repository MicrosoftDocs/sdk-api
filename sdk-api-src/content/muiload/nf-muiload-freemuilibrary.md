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

# FreeMUILibrary function


## -description


Releases the handle to a resource module loaded by <a href="https://msdn.microsoft.com/277067d8-c38d-4e79-9c1a-4e4af1987228">LoadMUILibrary</a>.


## -parameters




### -param hResModule [in]

Handle to a resource module loaded by <a href="https://msdn.microsoft.com/277067d8-c38d-4e79-9c1a-4e4af1987228">LoadMUILibrary</a>. The handle indicates either a language-specific resource file or an LN file.


## -returns



Returns <b>TRUE</b> if successful or <b>FALSE</b> otherwise. To get extended error information, the application can call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. The error code is the same as that returned by <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>.




## -remarks



Once the application has called <b>FreeMUILibrary</b>, it should treat the passed module handle as invalid.

Applications using this function can be built on pre-Windows Vista operating systems, but they must link statically with the MUILoad library provided in the Microsoft Windows SDK for Windows Vista.

<b>FreeMUILibrary</b> is related to <a href="https://msdn.microsoft.com/277067d8-c38d-4e79-9c1a-4e4af1987228">LoadMUILibrary</a> in the same way that <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a> is related to <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a>, and similar considerations need to be applied to its usage. In particular, to support correct reference counting, <b>FreeMUILibrary</b> should be called for any handle returned by <b>LoadMUILibrary</b>. For more information see the Remarks sections of <a href="https://msdn.microsoft.com/4fc699ca-6ffb-4954-9b72-1b827d558563">LoadLibraryEx</a> and <a href="https://msdn.microsoft.com/823d3147-4ba8-4fe5-ade4-e5604f47eb0a">FreeLibrary</a>.




## -see-also




<a href="https://msdn.microsoft.com/277067d8-c38d-4e79-9c1a-4e4af1987228">LoadMUILibrary</a>



<a href="https://msdn.microsoft.com/2980365c-5a83-4c0f-aa37-e212ec9f0408">Multilingual User Interface</a>



<a href="https://msdn.microsoft.com/918d1f04-78fe-4b60-bee7-08d2f131437e">Multilingual User Interface Functions</a>
 

 

