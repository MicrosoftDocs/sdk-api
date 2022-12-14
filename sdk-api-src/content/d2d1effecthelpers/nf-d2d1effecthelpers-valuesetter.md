---
UID: NF:d2d1effecthelpers.ValueSetter
title: ValueSetter function (d2d1effecthelpers.h)
description: Calls a member-function property setter callback for a value-type property. (ValueSetter)
helpviewer_keywords: ["ValueSetter","ValueSetter function [Direct2D]","d2d1effecthelpers/ValueSetter","direct2d.valuesetter"]
old-location: direct2d\valuesetter.htm
tech.root: Direct2D
ms.assetid: 5137D54E-1BAC-470C-AF16-0FB19DD36A61
ms.date: 12/05/2018
ms.keywords: ValueSetter, ValueSetter function [Direct2D], d2d1effecthelpers/ValueSetter, direct2d.valuesetter
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
 - ValueSetter
 - d2d1effecthelpers/ValueSetter
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
 - ValueSetter
---

# ValueSetter function


## -description

Calls a member-function property setter callback for a value-type property.

## -parameters

### -param effect [in]

The effect with the property.

### -param data [in]

When this method returns, contains a pointer to the data requested.

### -param dataSize

The number of bytes in the data to be retrieved.

### -param unnamedParam4

TBD

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

