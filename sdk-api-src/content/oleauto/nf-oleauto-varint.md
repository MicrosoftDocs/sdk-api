---
UID: NF:oleauto.VarInt
title: VarInt function (oleauto.h)
description: Returns the integer portion of a variant. (VarInt)
helpviewer_keywords: ["VarInt","VarInt function [Automation]","_oa96_VarInt","automat.varint","oleauto/VarInt"]
old-location: automat\varint.htm
tech.root: automat
ms.assetid: 96a9a158-d822-4cde-80c5-ea66f0fa4f1f
ms.date: 12/05/2018
ms.keywords: VarInt, VarInt function [Automation], _oa96_VarInt, automat.varint, oleauto/VarInt
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
 - VarInt
 - oleauto/VarInt
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
 - VarInt
---

# VarInt function


## -description

Returns the integer portion of a variant.

## -parameters

### -param pvarIn [in]

The variant.

### -param pvarResult [out]

The result variant.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the variant is negative, then the first negative integer less than or equal to the variant is returned.

