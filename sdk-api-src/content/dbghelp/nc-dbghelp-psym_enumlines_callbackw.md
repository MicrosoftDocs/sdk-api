---
UID: NC:dbghelp.PSYM_ENUMLINES_CALLBACKW
title: PSYM_ENUMLINES_CALLBACKW
author: windows-sdk-content
description: An application-defined callback function used with the SymEnumLines and SymEnumSourceLines functions.
old-location: base\symenumlinesproc.htm
old-project: debug
ms.assetid: 7379dd04-72a4-45b6-b02a-d3e8a5aaf0d7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PSYM_ENUMLINES_CALLBACK, PSYM_ENUMLINES_CALLBACKW, SymEnumLinesProc, SymEnumLinesProc callback, SymEnumLinesProc callback function, base.symenumlinesproc, dbghelp/SymEnumLinesProc
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
tech.root: 
req.typenames: DAV_CALLBACK_CRED, *PDAV_CALLBACK_CRED
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - DbgHelp.h
api_name:
 - SymEnumLinesProc
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# PSYM_ENUMLINES_CALLBACKW callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/d518b320-e4db-4bd1-8221-583eb84c292c">SymEnumLines</a> and <a href="https://msdn.microsoft.com/395dd97b-4d0b-4f55-80af-38fc748c924a">SymEnumSourceLines</a> functions.

The <b>PSYM_ENUMLINES_CALLBACK</b> and <b>PSYM_ENUMLINES_CALLBACKW</b> types define a pointer to this callback function. 
<b>SymEnumLinesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param LineInfo [in]

A pointer to a 
<a href="https://msdn.microsoft.com/8a2ee743-d2e8-402a-b659-0c0b75052d1d">SRCCODEINFO</a> structure that provides information about the line.


### -param UserContext [in]

The user-defined value passed from the 
<a href="https://msdn.microsoft.com/d518b320-e4db-4bd1-8221-583eb84c292c">SymEnumLines</a> function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.


## -returns



If the function returns <b>TRUE</b>, the enumeration will continue.

If the function returns <b>FALSE</b>, the enumeration will stop.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/d518b320-e4db-4bd1-8221-583eb84c292c">SymEnumLines</a>



<a href="https://msdn.microsoft.com/395dd97b-4d0b-4f55-80af-38fc748c924a">SymEnumSourceLines</a>
 

 

