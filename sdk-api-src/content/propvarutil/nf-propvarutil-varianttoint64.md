---
UID: NF:propvarutil.VariantToInt64
title: VariantToInt64 function (propvarutil.h)
description: Extracts an Int64 property value of a variant structure. If no value can be extracted, then a default value is assigned.
helpviewer_keywords: ["VariantToInt64","VariantToInt64 function [Windows Properties]","_shell_VariantToInt64","properties.VariantToInt64","propvarutil/VariantToInt64","shell.VariantToInt64"]
old-location: properties\VariantToInt64.htm
tech.root: properties
ms.assetid: 5b8b4f93-dff1-40ef-9f99-c108a0b1bf70
ms.date: 12/05/2018
ms.keywords: VariantToInt64, VariantToInt64 function [Windows Properties], _shell_VariantToInt64, properties.VariantToInt64, propvarutil/VariantToInt64, shell.VariantToInt64
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - VariantToInt64
 - propvarutil/VariantToInt64
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - VariantToInt64
---

# VariantToInt64 function


## -description

Extracts an <b>Int64</b> property value of a variant structure. If no value can be extracted, then a default value is assigned.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param pllRet [out]

Type: <b>LONGLONG*</b>

Pointer to the extracted property value if one exists; otherwise, 0.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

