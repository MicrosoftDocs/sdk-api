---
UID: NF:oleauto.SafeArrayCreateVector
title: SafeArrayCreateVector function (oleauto.h)
description: Creates a one-dimensional array. A safe array created with SafeArrayCreateVector is a fixed size, so the constant FADF_FIXEDSIZE is always set.
helpviewer_keywords: ["SafeArrayCreateVector","SafeArrayCreateVector function [Automation]","_oa96_SafeArrayCreateVector","automat.safearraycreatevector","oleauto/SafeArrayCreateVector"]
old-location: automat\safearraycreatevector.htm
tech.root: automat
ms.assetid: b794b8c6-a523-4636-8681-a936dff3fc6f
ms.date: 12/05/2018
ms.keywords: SafeArrayCreateVector, SafeArrayCreateVector function [Automation], _oa96_SafeArrayCreateVector, automat.safearraycreatevector, oleauto/SafeArrayCreateVector
req.header: oleauto.h
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayCreateVector
 - oleauto/SafeArrayCreateVector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayCreateVector
---

# SafeArrayCreateVector function


## -description

Creates a one-dimensional array. A safe array created with <b>SafeArrayCreateVector</b> is a fixed size, so the constant FADF_FIXEDSIZE is always set.

## -parameters

### -param vt [in]

The base type of the array (the VARTYPE of each element of the array). The VARTYPE is restricted to a subset of the variant types. Neither the VT_ARRAY nor the VT_BYREF flag can be set. VT_EMPTY and VT_NULL are not valid base types for the array. All other types are legal.

### -param lLbound [in]

The lower bound for the array. This parameter can be negative.

### -param cElements [in]

The number of elements in the array.

## -returns

A safe array descriptor, or null if the array could not be created.

## -see-also

<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>



<a href="/windows/desktop/api/oleauto/nf-oleauto-safearraydestroy">SafeArrayDestroy</a>