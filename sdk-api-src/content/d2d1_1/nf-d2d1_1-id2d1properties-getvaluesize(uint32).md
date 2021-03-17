---
UID: NF:d2d1_1.ID2D1Properties.GetValueSize(UINT32)
title: ID2D1Properties::GetValueSize (d2d1_1.h)
description: Gets the size of the property value in bytes, using the property index.
helpviewer_keywords: ["GetValueSize","GetValueSize method [Direct2D]","GetValueSize method [Direct2D]","ID2D1Properties interface","ID2D1Properties interface [Direct2D]","GetValueSize method","ID2D1Properties.GetValueSize","ID2D1Properties::GetValueSize","ID2D1Properties::GetValueSize(UINT32)","d2d1_1/ID2D1Properties::GetValueSize","direct2d.id2d1properties_getvaluesize"]
old-location: direct2d\id2d1properties_getvaluesize.htm
tech.root: Direct2D
ms.assetid: fd65a610-9552-4efe-9050-715cb672acc8
ms.date: 12/05/2018
ms.keywords: GetValueSize, GetValueSize method [Direct2D], GetValueSize method [Direct2D],ID2D1Properties interface, ID2D1Properties interface [Direct2D],GetValueSize method, ID2D1Properties.GetValueSize, ID2D1Properties::GetValueSize, ID2D1Properties::GetValueSize(UINT32), d2d1_1/ID2D1Properties::GetValueSize, direct2d.id2d1properties_getvaluesize
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Properties::GetValueSize
 - d2d1_1/ID2D1Properties::GetValueSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Properties.GetValueSize
---

# ID2D1Properties::GetValueSize


## -description

Gets the size of the property value in bytes, using the property index.

## -parameters

### -param index

Type: <b>UINT32</b>

The index of the property.

## -returns

Type: <b>UINT32</b>

This method returns size of the value in bytes, using the property index

## -remarks

This method returns zero if <i>index</i> does not exist.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1properties">ID2D1Properties</a>