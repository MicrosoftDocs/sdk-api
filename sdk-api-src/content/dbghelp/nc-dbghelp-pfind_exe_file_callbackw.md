---
UID: NC:dbghelp.PFIND_EXE_FILE_CALLBACKW
title: PFIND_EXE_FILE_CALLBACKW
author: windows-sdk-content
description: An application-defined callback function used with the FindExecutableImageEx function. It verifies whether the executable file found by FindExecutableImageEx is the correct executable file.
old-location: base\findexecutableimageproc.htm
tech.root: debug
ms.assetid: cbd8cd63-8fdb-4314-8737-9f934de74f89
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FindExecutableImageProc, FindExecutableImageProc callback, FindExecutableImageProc callback function, PFIND_EXE_FILE_CALLBACK, PFIND_EXE_FILE_CALLBACKW, _win32_findexecutableimageproc, base.findexecutableimageproc, dbghelp/FindExecutableImageProc
ms.topic: callback
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - FindExecutableImageProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# PFIND_EXE_FILE_CALLBACKW callback function


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
 

 

