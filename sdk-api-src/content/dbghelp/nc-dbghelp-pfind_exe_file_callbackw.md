---
UID: NC:dbghelp.PFIND_EXE_FILE_CALLBACKW
title: PFIND_EXE_FILE_CALLBACKW
author: windows-driver-content
description: An application-defined callback function used with the FindExecutableImageEx function. It verifies whether the executable file found by FindExecutableImageEx is the correct executable file.
old-location: base\findexecutableimageproc.htm
old-project: Debug
ms.assetid: cbd8cd63-8fdb-4314-8737-9f934de74f89
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: FindExecutableImageProc, FindExecutableImageProc callback, FindExecutableImageProc callback function, PFIND_EXE_FILE_CALLBACK, PFIND_EXE_FILE_CALLBACKW, _win32_findexecutableimageproc, base.findexecutableimageproc, dbghelp/FindExecutableImageProc
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: DAV_CALLBACK_CRED, *PDAV_CALLBACK_CRED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	DbgHelp.h
api_name:
-	FindExecutableImageProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

