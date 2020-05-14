---
UID: NC:dbghelp.PFINDFILEINPATHCALLBACKW
title: PFINDFILEINPATHCALLBACKW (dbghelp.h)
description: An application-defined callback function used with the SymFindFileInPath function.helpviewer_keywords: ["PFINDFILEINPATHCALLBACK","PFINDFILEINPATHCALLBACKW","SymFindFileInPathProc","SymFindFileInPathProc callback","SymFindFileInPathProc callback function","_win32_symfindfileinpathproc","base.symfindfileinpathproc","dbghelp/SymFindFileInPathProc"]
old-location: base\symfindfileinpathproc.htm
tech.root: Debug
ms.assetid: e579158e-053d-4c81-a2c3-ac3af3d3a201
ms.date: 12/05/2018
ms.keywords: PFINDFILEINPATHCALLBACK, PFINDFILEINPATHCALLBACKW, SymFindFileInPathProc, SymFindFileInPathProc callback, SymFindFileInPathProc callback function, _win32_symfindfileinpathproc, base.symfindfileinpathproc, dbghelp/SymFindFileInPathProc
f1_keywords:
- dbghelp/SymFindFileInPathProc
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
---

# PFINDFILEINPATHCALLBACKW callback function


## -description


An application-defined callback function used with the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a> function.

The <b>PFINDFILEINPATHCALLBACK</b> and <b>PFINDFILEINPATHCALLBACKW</b> types define a pointer to this callback function. 
<b>SymFindFileInPathProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param filename


### -param context [in]

The user-defined value specified in 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a>, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides some context for the callback function.


#### - fileName [in]

The name of the file located by <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a>.


## -returns



Return <b>TRUE</b> to continue searching.

Return <b>FALSE</b> to end the search.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symfindfileinpath">SymFindFileInPath</a>
 

 

