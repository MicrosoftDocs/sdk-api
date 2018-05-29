---
UID: NF:d2d1effecthelpers.StringSetter
title: StringSetter function
author: windows-sdk-content
description: Calls a member-function property setter callback for a string-type property.
old-location: direct2d\stringsetter.htm
old-project: Direct2D
ms.assetid: 6BCDB312-13D8-47EA-BB88-4172C3A02DBE
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: StringSetter, StringSetter function [Direct2D], d2d1effecthelpers/StringSetter, direct2d.stringsetter
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: D2D1_VERTEX_RANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	d2d1.dll
api_name:
-	StringSetter
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# StringSetter function


## -description


Calls a member-function property setter callback for a string-type property.


## -parameters




### -param effect [in]

Type: <b>IUnknown*</b>

The effect with the property.


### -param data [in]

Type: <b>const BYTE*</b>

When this method returns, contains a pointer to the data requested.


### -param dataSize

Type: <b>UINT32</b>

The number of bytes in the data to be retrieved.


### -param param

TBD




## -returns



Type: <b>HRESULT CALLBACK</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



