---
UID: NF:d2d1effecthelpers.ValueGetter
title: ValueGetter function
author: windows-sdk-content
description: Calls a member-function property setter callback for a value-type property.
old-location: direct2d\valuegetter.htm
tech.root: Direct2D
ms.assetid: F811E606-461A-4D18-B49B-3DD11BF991BC
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ValueGetter, ValueGetter function [Direct2D], d2d1effecthelpers/ValueGetter, direct2d.valuegetter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d2d1.dll
api_name:
 - ValueGetter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- ValueGetter
: 
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


### -param arg5

TBD




## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



