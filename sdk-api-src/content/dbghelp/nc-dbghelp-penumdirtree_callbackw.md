---
UID: NC:dbghelp.PENUMDIRTREE_CALLBACKW
title: PENUMDIRTREE_CALLBACKW
author: windows-sdk-content
description: An application-defined callback function used with the EnumDirTree function. It is called every time a match is found.
old-location: base\enumdirtreeproc.htm
tech.root: Debug
ms.assetid: eae41b83-bba5-4656-9a5c-b6ef56845954
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EnumDirTreeProc, EnumDirTreeProc callback, EnumDirTreeProc callback function, PENUMDIRTREE_CALLBACK, PENUMDIRTREE_CALLBACKW, _win32_enumdirtreeproc, base.enumdirtreeproc, dbghelp/EnumDirTreeProc
ms.prod: windows
ms.technology: windows-sdk
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
 - EnumDirTreeProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.0 or later
---

# PENUMDIRTREE_CALLBACKW callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/2dd132f3-83d4-4afd-b44d-9f8d385d6116">EnumDirTree</a> function. It is called every time a match is found.

The <b>PENUMDIRTREE_CALLBACK</b> and <b>PENUMDIRTREE_CALLBACKW</b> types define a pointer to this callback function. 
<i>EnumDirTreeProc</i> is a placeholder for the application-defined function name.


## -parameters




### -param FilePath [in]

A pointer to a buffer that receives the full path of the file that is found.


### -param CallerData [in, optional]

A user-defined value specified in 
<a href="https://msdn.microsoft.com/2dd132f3-83d4-4afd-b44d-9f8d385d6116">EnumDirTree</a>, or <b>NULL</b>. Typically, this parameter is used by an application to pass a pointer to a data structure that enables the callback function to establish some context.


## -returns



To continue enumeration, the callback function must return <b>FALSE</b>.

To stop enumeration, the callback function must return <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/2dd132f3-83d4-4afd-b44d-9f8d385d6116">EnumDirTree</a>
 

 

