---
UID: NF:propvarutil.VariantToString
title: VariantToString function (propvarutil.h)
description: Extracts the variant value of a variant structure to a string. If no value can be extracted, then a default value is assigned.
helpviewer_keywords: ["VariantToString","VariantToString function [Windows Properties]","_shell_VariantToString","properties.VariantToString","propvarutil/VariantToString","shell.VariantToString"]
old-location: properties\VariantToString.htm
tech.root: properties
ms.assetid: 4850f9b8-8f86-4428-bf3b-f3abdc6047c1
ms.date: 12/05/2018
ms.keywords: VariantToString, VariantToString function [Windows Properties], _shell_VariantToString, properties.VariantToString, propvarutil/VariantToString, shell.VariantToString
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
 - VariantToString
 - propvarutil/VariantToString
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
 - VariantToString
---

# VariantToString function


## -description

Extracts the variant value of a variant structure to a string. If no value can be extracted, then a default value is assigned.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param pszBuf [out]

Type: <b>PWSTR</b>

Pointer to the extracted property value if one exists; otherwise, empty.

### -param cchBuf [in]

Type: <b>UINT</b>

Specifies string length, in characters.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

