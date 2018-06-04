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

# PFIND_EXE_FILE_CALLBACK callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/7571e168-2e91-4c97-9139-8225d28cc399">FindExecutableImageEx</a> function. It verifies whether the executable file found by 
<b>FindExecutableImageEx</b> is the correct executable file.

The <b>PFIND_EXE_FILE_CALLBACK</b> and <b>PFIND_EXE_FILE_CALLBACKW</b> types define a pointer to this callback function. 
<b>FindExecutableImageProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param FileHandle [in]

A handle to the executable file.


### -param FileName [in]

The name of the executable file.


### -param CallerData [in]

Optional user-defined data. This parameter can be <b>NULL</b>.


## -returns



If the executable file is valid, return <b>TRUE</b>. Otherwise, return <b>FALSE</b>.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/7571e168-2e91-4c97-9139-8225d28cc399">FindExecutableImageEx</a>
 

 

