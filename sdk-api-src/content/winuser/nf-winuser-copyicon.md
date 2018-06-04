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

# CopyIcon function


## -description


Copies the specified icon from another module to the current module.


## -parameters




### -param hIcon [in]

Type: <b>HICON</b>

A handle to the icon to be copied.


## -returns



Type: <b>HICON</b>

If the function succeeds, the return value is a handle to the duplicate icon.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



The <b>CopyIcon</b> function enables an application or DLL to get its own handle to an icon owned by another module. If the other module is freed, the application icon will still be able to use the icon. 

Before closing, an application must call the <a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a> function to free any system resources associated with the icon.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/2ae1ee3e-5114-4712-a2a8-b413b83bb58c">CopyCursor</a>



<a href="https://msdn.microsoft.com/ffe21e34-ebe0-4ec8-830f-64c733ef9097">DestroyIcon</a>



<a href="https://msdn.microsoft.com/9c36ec22-45d3-4ed4-93d3-46a24d5fc5f9">DrawIcon</a>



<a href="https://msdn.microsoft.com/037005b4-e9b2-483a-b277-7abd53a44b99">DrawIconEx</a>



<a href="https://msdn.microsoft.com/1dc588f4-b032-40a8-82ef-5b9fc04abb0b">Icons</a>



<b>Reference</b>
 

 

