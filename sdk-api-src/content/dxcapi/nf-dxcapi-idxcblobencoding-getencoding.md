---
UID: NF:dxcapi.IDxcBlobEncoding.GetEncoding
tech.root: direct3dhlsl
title: IDxcBlobEncoding::GetEncoding
ms.date: 04/05/2023
targetos: Windows
description: Retrieve the encoding for this blob.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dxcapi.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - dxcapi.h
api_name:
 - IDxcBlobEncoding::GetEncoding
f1_keywords:
 - IDxcBlobEncoding::GetEncoding
 - dxcapi/IDxcBlobEncoding::GetEncoding
dev_langs:
 - c++
helpviewer_keywords:
 - GetEncoding
---

## -description

Retrieve the encoding for this blob.

## -parameters

### -param pKnown

Pointer to a variable that will be set to `TRUE` if the encoding is known.

### -param pCodePage

Pointer to a variable that will be set to the encoding used for this blob. If the encoding isn't known then *pCodePage* will be set to **CP_ACP**.

## -returns

## -remarks

## -see-also
