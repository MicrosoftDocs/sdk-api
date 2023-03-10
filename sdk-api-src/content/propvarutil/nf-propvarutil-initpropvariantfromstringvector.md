---
UID: NF:propvarutil.InitPropVariantFromStringVector
title: InitPropVariantFromStringVector function (propvarutil.h)
description: Initializes a PROPVARIANT structure from a specified string vector.
helpviewer_keywords: ["InitPropVariantFromStringVector","InitPropVariantFromStringVector function [Windows Properties]","properties.InitPropVariantFromStringVector","propvarutil/InitPropVariantFromStringVector","shell.InitPropVariantFromStringVector","shell_InitPropVariantFromStringVector"]
old-location: properties\InitPropVariantFromStringVector.htm
tech.root: properties
ms.assetid: 4190337f-f9f6-4584-b667-6b96c1ce48c8
ms.date: 12/05/2018
ms.keywords: InitPropVariantFromStringVector, InitPropVariantFromStringVector function [Windows Properties], properties.InitPropVariantFromStringVector, propvarutil/InitPropVariantFromStringVector, shell.InitPropVariantFromStringVector, shell_InitPropVariantFromStringVector
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
 - InitPropVariantFromStringVector
 - propvarutil/InitPropVariantFromStringVector
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
 - InitPropVariantFromStringVector
---

# InitPropVariantFromStringVector function


## -description

Initializes a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure from a specified string vector.

## -parameters

### -param prgsz [in]

Type: <b>PCWSTR*</b>

Pointer to a buffer that contains the source string vector.

### -param cElems [in]

Type: <b>ULONG</b>

The number of vector elements in <i>prgsz</i>.

### -param ppropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>HRESULT</b>

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstring">InitPropVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstringasvector">InitPropVariantFromStringAsVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initvariantfromstring">InitVariantFromString</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringvector">PropVariantToStringVector</a>