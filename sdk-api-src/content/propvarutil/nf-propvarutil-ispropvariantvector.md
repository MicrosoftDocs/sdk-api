---
UID: NF:propvarutil.IsPropVariantVector
title: IsPropVariantVector function (propvarutil.h)
description: Specifies whether a PROPVARIANT structure has a vector type.
helpviewer_keywords: ["IsPropVariantVector","IsPropVariantVector function [Windows Properties]","properties.IsPropVariantVector","propvarutil/IsPropVariantVector","shell.IsPropVariantVector","shell_IsPropVariantVector"]
old-location: properties\IsPropVariantVector.htm
tech.root: properties
ms.assetid: c094c636-e51d-4a61-8d92-90abe2f0446e
ms.date: 12/05/2018
ms.keywords: IsPropVariantVector, IsPropVariantVector function [Windows Properties], properties.IsPropVariantVector, propvarutil/IsPropVariantVector, shell.IsPropVariantVector, shell_IsPropVariantVector
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
 - IsPropVariantVector
 - propvarutil/IsPropVariantVector
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
 - IsPropVariantVector
---

# IsPropVariantVector function


## -description

Specifies whether a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure has a vector type.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure being queried.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>propvar</i> is a VT_ARRAY | VT_VECTOR <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>; otherwise, <b>FALSE</b>.

## -remarks

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.