---
UID: NF:d2d1effecthelpers.ValueGetter
title: ValueGetter function (d2d1effecthelpers.h)
description: Calls a member-function property setter callback for a value-type property. (ValueGetter)
helpviewer_keywords: ["ValueGetter","ValueGetter function [Direct2D]","d2d1effecthelpers/ValueGetter","direct2d.valuegetter"]
old-location: direct2d\valuegetter.htm
tech.root: Direct2D
ms.assetid: F811E606-461A-4D18-B49B-3DD11BF991BC
ms.date: 12/05/2018
ms.keywords: ValueGetter, ValueGetter function [Direct2D], d2d1effecthelpers/ValueGetter, direct2d.valuegetter
req.header: d2d1effecthelpers.h
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
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ValueGetter
 - d2d1effecthelpers/ValueGetter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d2d1.dll
api_name:
 - ValueGetter
---

# ValueGetter function


## -description

Calls a member-function property setter callback for a value-type property.

## -parameters

### -param effect [in]

The effect with the property.

### -param data [out, optional]

When this method returns, contains a pointer to the data requested.

### -param dataSize

The number of bytes in the data to be retrieved.

### -param actualSize [out, optional]

The actual size of the data, if the data is not measured in bytes.

### -param unnamedParam5

TBD

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

