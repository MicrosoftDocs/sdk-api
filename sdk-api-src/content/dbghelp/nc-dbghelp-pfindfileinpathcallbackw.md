---
UID: NC:dbghelp.PFINDFILEINPATHCALLBACKW
title: PFINDFILEINPATHCALLBACKW (dbghelp.h)
author: windows-sdk-content
description: An application-defined callback function used with the SymFindFileInPath function.
old-location: base\symfindfileinpathproc.htm
tech.root: Debug
ms.assetid: e579158e-053d-4c81-a2c3-ac3af3d3a201
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PFINDFILEINPATHCALLBACK, PFINDFILEINPATHCALLBACKW, SymFindFileInPathProc, SymFindFileInPathProc callback, SymFindFileInPathProc callback function, _win32_symfindfileinpathproc, base.symfindfileinpathproc, dbghelp/SymFindFileInPathProc
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
 - SymFindFileInPathProc
product: Windows
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
---

# PFINDFILEINPATHCALLBACKW callback function


## -description


An application-defined callback function used with the 
<a href="https://msdn.microsoft.com/f85d8cd9-958a-490a-b155-3a9abdeda922">SymFindFileInPath</a> function.

The <b>PFINDFILEINPATHCALLBACK</b> and <b>PFINDFILEINPATHCALLBACKW</b> types define a pointer to this callback function. 
<b>SymFindFileInPathProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param filename


### -param context [in]

The user-defined value specified in 
<a href="https://msdn.microsoft.com/f85d8cd9-958a-490a-b155-3a9abdeda922">SymFindFileInPath</a>, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides some context for the callback function.


#### - fileName [in]

The name of the file located by <a href="https://msdn.microsoft.com/f85d8cd9-958a-490a-b155-3a9abdeda922">SymFindFileInPath</a>.


## -returns



Return <b>TRUE</b> to continue searching.

Return <b>FALSE</b> to end the search.




## -see-also




<a href="https://msdn.microsoft.com/7b28f70b-2d97-4cc2-8064-dfb806f9cffa">DbgHelp Functions</a>



<a href="https://msdn.microsoft.com/f85d8cd9-958a-490a-b155-3a9abdeda922">SymFindFileInPath</a>
 

 

