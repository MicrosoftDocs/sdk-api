---
UID: NC:dbghelp.PSYM_ENUMLINES_CALLBACKW
title: PSYM_ENUMLINES_CALLBACKW (dbghelp.h)
description: An application-defined callback function used with the SymEnumLines and SymEnumSourceLines functions.helpviewer_keywords: ["PSYM_ENUMLINES_CALLBACK","PSYM_ENUMLINES_CALLBACKW","SymEnumLinesProc","SymEnumLinesProc callback","SymEnumLinesProc callback function","base.symenumlinesproc","dbghelp/SymEnumLinesProc"]
old-location: base\symenumlinesproc.htm
tech.root: Debug
ms.assetid: 7379dd04-72a4-45b6-b02a-d3e8a5aaf0d7
ms.date: 12/05/2018
ms.keywords: PSYM_ENUMLINES_CALLBACK, PSYM_ENUMLINES_CALLBACKW, SymEnumLinesProc, SymEnumLinesProc callback, SymEnumLinesProc callback function, base.symenumlinesproc, dbghelp/SymEnumLinesProc
f1_keywords:
- dbghelp/SymEnumLinesProc
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
- SymEnumLinesProc
targetos: Windows
req.typenames: 
req.redist: DbgHelp.dll 6.1 or later
ms.custom: 19H1
---

# PSYM_ENUMLINES_CALLBACKW callback function


## -description


An application-defined callback function used with the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symenumlines">SymEnumLines</a> and <a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcelines">SymEnumSourceLines</a> functions.

The <b>PSYM_ENUMLINES_CALLBACK</b> and <b>PSYM_ENUMLINES_CALLBACKW</b> types define a pointer to this callback function. 
<b>SymEnumLinesProc</b> is a placeholder for the application-defined function name.


## -parameters




### -param LineInfo [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/ns-dbghelp-srccodeinfo">SRCCODEINFO</a> structure that provides information about the line.


### -param UserContext [in]

The user-defined value passed from the 
<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symenumlines">SymEnumLines</a> function, or <b>NULL</b>. This parameter is typically used by an application to pass a pointer to a data structure that provides context information for the callback function.


## -returns



If the function returns <b>TRUE</b>, the enumeration will continue.

If the function returns <b>FALSE</b>, the enumeration will stop.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Debug/dbghelp-functions">DbgHelp Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symenumlines">SymEnumLines</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nf-dbghelp-symenumsourcelines">SymEnumSourceLines</a>
 

 

