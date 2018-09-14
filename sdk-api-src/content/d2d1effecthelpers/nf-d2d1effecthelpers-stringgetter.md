---
UID: NF:d2d1effecthelpers.StringGetter
title: StringGetter function
author: windows-sdk-content
description: Calls a member-function property getter callback for a string-type property.
old-location: direct2d\stringgetter.htm
tech.root: Direct2D
ms.assetid: 9C35AF38-1937-46DD-8DC4-BBA322E5CAAA
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: StringGetter, StringGetter function [Direct2D], d2d1effecthelpers/StringGetter, direct2d.stringgetter
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
 - StringGetter
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StringGetter function


## -description


Calls a member-function property getter callback for a string-type property.


## -parameters




### -param effect [in]

Type: <b>const IUnknown*</b>

The effect with the property.


### -param data [out, optional]

Type: <b>BYTE*</b>

When this method returns, contains a pointer to the data requested.


### -param dataSize

Type: <b>UINT32</b>

The number of bytes in the data to be retrieved.


### -param actualSize [out, optional]

Type: <b>UINT32*</b>

The actual size of the data, if the data is not measured in bytes.


### -param arg1

TBD




## -returns



Type: <b>HRESULT CALLBACK</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



