---
UID: NF:propvarutil.VariantGetStringElem
title: VariantGetStringElem function (propvarutil.h)
description: Extracts a single wide string element from a variant structure.
helpviewer_keywords: ["VariantGetStringElem","VariantGetStringElem function [Windows Properties]","_shell_VariantGetStringElem","properties.VariantGetStringElem","propvarutil/VariantGetStringElem","shell.VariantGetStringElem"]
old-location: properties\VariantGetStringElem.htm
tech.root: properties
ms.assetid: c4d1a37e-f7d1-4c0e-8d05-93a0153f2878
ms.date: 12/05/2018
ms.keywords: VariantGetStringElem, VariantGetStringElem function [Windows Properties], _shell_VariantGetStringElem, properties.VariantGetStringElem, propvarutil/VariantGetStringElem, shell.VariantGetStringElem
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
 - VariantGetStringElem
 - propvarutil/VariantGetStringElem
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
 - VariantGetStringElem
---

# VariantGetStringElem function


## -description

Extracts a single wide string element from a variant structure.

## -parameters

### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param iElem [in]

Type: <b>ULONG</b>

Specifies a vector or array index; otherwise, value must be 0.

### -param ppszVal [out]

Type: <b>PWSTR*</b>

The address of a pointer to the extracted element value.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

