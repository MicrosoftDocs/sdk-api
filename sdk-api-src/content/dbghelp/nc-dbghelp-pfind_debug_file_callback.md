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

# PFIND_DEBUG_FILE_CALLBACK callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/1e89fe9a-4631-42b9-96ee-90393b4d9084">FindDebugInfoFileEx</a> function. It verifies whether the symbol file located by 
<b>FindDebugInfoFileEx</b> is the correct symbol file.

The <b>PFIND_DEBUG_FILE_CALLBACK</b> and <b>PFIND_DEBUG_FILE_CALLBACKW</b> types define a pointer to this callback function. 
<b>FindDebugInfoFileProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param FileHandle [in]

A handle to the symbol file.


### -param FileName [in]

The name of the symbol file.


### -param CallerData [in]

Optional user-defined data. This parameter can be <b>NULL</b>.


## -returns



If the symbol file is valid, return <b>TRUE</b>. Otherwise, return <b>FALSE</b>.




## -remarks



One way to verify the symbol file is to compare its timestamp to the timestamp in the image. To retrieve the timestamp of the image, use the 
<a href="https://msdn.microsoft.com/9ce7b211-5447-4624-b197-85730c4a7a10">GetTimestampForLoadedLibrary</a> function. To retrieve the timestamp of the symbol file, use the 
<a href="https://msdn.microsoft.com/e8057cb5-3331-4460-b07c-4338a57024be">SymGetModuleInfo64</a> function.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/1e89fe9a-4631-42b9-96ee-90393b4d9084">FindDebugInfoFileEx</a>



<a href="https://msdn.microsoft.com/9ce7b211-5447-4624-b197-85730c4a7a10">GetTimestampForLoadedLibrary</a>



<a href="https://msdn.microsoft.com/e8057cb5-3331-4460-b07c-4338a57024be">SymGetModuleInfo64</a>
 

 

