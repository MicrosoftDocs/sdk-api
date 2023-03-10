---
UID: NF:propvarutil.IsPropVariantString
title: IsPropVariantString function (propvarutil.h)
description: Specifies whether a specified PROPVARIANT structure is a string type.
helpviewer_keywords: ["IsPropVariantString","IsPropVariantString function [Windows Properties]","properties.IsPropVariantString","propvarutil/IsPropVariantString","shell.IsPropVariantString","shell_IsPropVariantString"]
old-location: properties\IsPropVariantString.htm
tech.root: properties
ms.assetid: 3f580098-6bfb-41bd-b43d-986ee00b9c75
ms.date: 12/05/2018
ms.keywords: IsPropVariantString, IsPropVariantString function [Windows Properties], properties.IsPropVariantString, propvarutil/IsPropVariantString, shell.IsPropVariantString, shell_IsPropVariantString
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
 - IsPropVariantString
 - propvarutil/IsPropVariantString
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
 - IsPropVariantString
---

# IsPropVariantString function


## -description

Specifies whether a specified <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure is a string type.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

## -returns

Type: <b>BOOL</b>

Returns <b>TRUE</b> if <i>propvar</i> is a VT_LPWSTR or VT_BSTR <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>; otherwise, <b>FALSE</b>.

## -remarks

If this function returns <b>TRUE</b>, the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure referenced in <i>propvar</i> contains a Unicode string. To retrieve it, call <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttostringwithdefault">PropVariantToStringWithDefault</a> as shown here:

                

<code>PropVariantToStringWithDefault(propvar, NULL);</code>

This is an inline function, with its source code provided in the header. It is not included in any .dll or .lib file.