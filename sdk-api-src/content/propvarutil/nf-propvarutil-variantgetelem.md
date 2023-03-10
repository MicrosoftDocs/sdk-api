---
UID: NF:propvarutil.VariantGetElem
title: VariantGetElem function (propvarutil.h)
description: Initializes a VARIANT structure from a specified variant element.
helpviewer_keywords: ["VariantGetElem","VariantGetElem function [Windows Properties]","_shell_VariantGetElem","properties.VariantGetElem","propvarutil/VariantGetElem","shell.VariantGetElem"]
old-location: properties\VariantGetElem.htm
tech.root: properties
ms.assetid: e1541e66-3ccc-494c-a909-72eeb9159d11
ms.date: 12/05/2018
ms.keywords: VariantGetElem, VariantGetElem function [Windows Properties], _shell_VariantGetElem, properties.VariantGetElem, propvarutil/VariantGetElem, shell.VariantGetElem
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - VariantGetElem
 - propvarutil/VariantGetElem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Propvarutil.h
api_name:
 - VariantGetElem
---

# VariantGetElem function


## -description

Initializes a <a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a> structure from a specified variant element.

## -parameters

### -param varIn [in]

Type: <b>REFVARIANT</b>

Reference to a source variant structure.

### -param iElem [in]

Type: <b>ULONG</b>

Specifies index of source variant structure element. If source structure is empty, then this parameter is not used.

### -param pvar [out]

Type: <b>VARIANT*</b>

Pointer to the values specified from the source variant structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.