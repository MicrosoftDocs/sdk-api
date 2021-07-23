---
UID: NF:propvarutil.VariantToGUID
title: VariantToGUID function (propvarutil.h)
description: Extracts a GUID property value of a variant structure.
helpviewer_keywords: ["VariantToGUID","VariantToGUID function [Windows Properties]","_shell_VariantToGUID","properties.VariantToGUID","propvarutil/VariantToGUID","shell.VariantToGUID"]
old-location: properties\VariantToGUID.htm
tech.root: properties
ms.assetid: 1af84b55-da7e-430c-97fe-1c544a40c039
ms.date: 12/05/2018
ms.keywords: VariantToGUID, VariantToGUID function [Windows Properties], _shell_VariantToGUID, properties.VariantToGUID, propvarutil/VariantToGUID, shell.VariantToGUID
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
 - VariantToGUID
 - propvarutil/VariantToGUID
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
 - VariantToGUID
---

# VariantToGUID function


## -description

Extracts a <b>GUID</b> property value of a variant structure.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param pguid [out]

Type: <b>GUID*</b>

Pointer to the extracted property value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

