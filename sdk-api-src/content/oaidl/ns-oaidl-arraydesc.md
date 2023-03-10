---
UID: NS:oaidl.tagARRAYDESC
title: ARRAYDESC (oaidl.h)
description: Describes an array, its element type, and its dimension.
helpviewer_keywords: ["ARRAYDESC","ARRAYDESC structure [Automation]","_oa96_ARRAYDESC","automat.arraydesc","oaidl/ARRAYDESC"]
old-location: automat\arraydesc.htm
tech.root: automat
ms.assetid: 5d48c9b7-a718-46bd-b8ba-5c92847c9a12
ms.date: 12/05/2018
ms.keywords: ARRAYDESC, ARRAYDESC structure [Automation], _oa96_ARRAYDESC, automat.arraydesc, oaidl/ARRAYDESC
req.header: oaidl.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ARRAYDESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagARRAYDESC
 - oaidl/tagARRAYDESC
 - ARRAYDESC
 - oaidl/ARRAYDESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OaIdl.h
api_name:
 - ARRAYDESC
---

# ARRAYDESC structure


## -description

Describes an array, its element type, and its dimension.

## -struct-fields

### -field tdescElem

The element type.

### -field cDims

The dimension count.

### -field rgbounds

A variable-length array containing one element for each dimension.

## -see-also

<a href="/windows/desktop/api/oaidl/ns-oaidl-typedesc">TYPEDESC</a>