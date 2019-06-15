---
UID: NS:dbghelp._SRCCODEINFOW
title: SRCCODEINFOW (dbghelp.h)
author: windows-sdk-content
description: Contains line information.
old-location: base\srccodeinfo_str.htm
tech.root: Debug
ms.assetid: 8a2ee743-d2e8-402a-b659-0c0b75052d1d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSRCCODEINFOW, PSRCCODEINFO, PSRCCODEINFO structure pointer, SRCCODEINFO, SRCCODEINFO structure, SRCCODEINFOW, _SRCCODEINFO, _SRCCODEINFOW, base.srccodeinfo_str, dbghelp/PSRCCODEINFO, dbghelp/SRCCODEINFO, dbghelp/SRCCODEINFOW"
ms.topic: struct
req.header: dbghelp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SRCCODEINFOW (Unicode) and SRCCODEINFO (ANSI)
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
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - SRCCODEINFO
 - SRCCODEINFO
 - SRCCODEINFOW
product: Windows
targetos: Windows
req.typenames: SRCCODEINFOW, *PSRCCODEINFOW
req.redist: DbgHelp.dll 6.1 or later
ms.custom: 19H1
---

# SRCCODEINFOW structure


## -description


Contains line information.


## -struct-fields




### -field SizeOfStruct

The size of the structure, in bytes.


### -field Key

This member is not used.


### -field ModBase

The base address of the module that contains the line.


### -field Obj

The name of the object file within the module that contains the line.


### -field FileName

The fully qualified source file name.


### -field LineNumber

The line number within the source file.


### -field Address

The virtual address of the first instruction of the line.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dbghelp/nc-dbghelp-psym_enumlines_callback">SymEnumLinesProc</a>
 

 

