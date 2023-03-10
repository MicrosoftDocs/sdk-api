---
UID: NF:propvarutil.VariantToUInt32
title: VariantToUInt32 function (propvarutil.h)
description: Extracts unsigned Int32 property value of a variant structure. If no value can be extracted, then a default value is assigned.
helpviewer_keywords: ["VariantToUInt32","VariantToUInt32 function [Windows Properties]","_shell_VariantToUInt32","properties.VariantToUInt32","propvarutil/VariantToUInt32","shell.VariantToUInt32"]
old-location: properties\VariantToUInt32.htm
tech.root: properties
ms.assetid: 24421477-8930-4c8f-8fee-5d8367123c7e
ms.date: 12/05/2018
ms.keywords: VariantToUInt32, VariantToUInt32 function [Windows Properties], _shell_VariantToUInt32, properties.VariantToUInt32, propvarutil/VariantToUInt32, shell.VariantToUInt32
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
 - VariantToUInt32
 - propvarutil/VariantToUInt32
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
 - VariantToUInt32
---

# VariantToUInt32 function


## -description

Extracts unsigned <b>Int32</b> property value of a variant structure. If no value can be extracted, then a default value is assigned.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param pulRet [out]

Type: <b>ULONG*</b>

Pointer to the extracted property value if one exists; otherwise, 0.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

