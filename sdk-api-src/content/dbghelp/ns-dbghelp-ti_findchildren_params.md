---
UID: NS:dbghelp._TI_FINDCHILDREN_PARAMS
title: TI_FINDCHILDREN_PARAMS (dbghelp.h)
description: Contains type index information. It is used by the SymGetTypeInfo function.
helpviewer_keywords: ["TI_FINDCHILDREN_PARAMS","TI_FINDCHILDREN_PARAMS structure","_TI_FINDCHILDREN_PARAMS","_win32_ti_findchildren_params_str","base.ti_findchildren_params_str","dbghelp/TI_FINDCHILDREN_PARAMS"]
old-location: base\ti_findchildren_params_str.htm
tech.root: Debug
ms.assetid: 618717d2-879d-4284-a4c2-0a5102698ed9
ms.date: 12/05/2018
ms.keywords: TI_FINDCHILDREN_PARAMS, TI_FINDCHILDREN_PARAMS structure, _TI_FINDCHILDREN_PARAMS, _win32_ti_findchildren_params_str, base.ti_findchildren_params_str, dbghelp/TI_FINDCHILDREN_PARAMS
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
targetos: Windows
req.typenames: TI_FINDCHILDREN_PARAMS
req.redist: DbgHelp.dll 5.1 or later
ms.custom: 19H1
f1_keywords:
 - _TI_FINDCHILDREN_PARAMS
 - dbghelp/_TI_FINDCHILDREN_PARAMS
 - TI_FINDCHILDREN_PARAMS
 - dbghelp/TI_FINDCHILDREN_PARAMS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DbgHelp.h
api_name:
 - TI_FINDCHILDREN_PARAMS
---

# TI_FINDCHILDREN_PARAMS structure


## -description

Contains type index information. It is used by the 
<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgettypeinfo">SymGetTypeInfo</a> function.

## -struct-fields

### -field Count

The number of children.

### -field Start

The zero-based index of the child from which the child indexes are to be retrieved. For example, in an array with five elements, if Start is two, this indicates the third array element. In most cases, this member is zero.

### -field ChildId

An array of type indexes. There is one index per child.

## -see-also

<a href="/windows/desktop/api/dbghelp/nf-dbghelp-symgettypeinfo">SymGetTypeInfo</a>