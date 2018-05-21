---
UID: NS:dbghelp._TI_FINDCHILDREN_PARAMS
title: "_TI_FINDCHILDREN_PARAMS"
author: windows-driver-content
description: Contains type index information. It is used by the SymGetTypeInfo function.
old-location: base\ti_findchildren_params_str.htm
old-project: Debug
ms.assetid: 618717d2-879d-4284-a4c2-0a5102698ed9
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: TI_FINDCHILDREN_PARAMS, TI_FINDCHILDREN_PARAMS structure, _TI_FINDCHILDREN_PARAMS, _win32_ti_findchildren_params_str, base.ti_findchildren_params_str, dbghelp/TI_FINDCHILDREN_PARAMS
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: TI_FINDCHILDREN_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	DbgHelp.h
api_name:
-	TI_FINDCHILDREN_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _TI_FINDCHILDREN_PARAMS structure


## -description


Contains type index information. It is used by the 
<a href="https://msdn.microsoft.com/bc94a5b1-d49d-425a-89a8-c584c3979930">SymGetTypeInfo</a> function.


## -struct-fields




### -field Count

The number of children.


### -field Start

The zero-based index of the child from which the child indexes are to be retrieved. For example, in an array with five elements, if Start is two, this indicates the third array element. In most cases, this member is zero.


### -field ChildId

An array of type indexes. There is one index per child.


## -see-also




<a href="https://msdn.microsoft.com/bc94a5b1-d49d-425a-89a8-c584c3979930">SymGetTypeInfo</a>
 

 

