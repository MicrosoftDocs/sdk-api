---
UID: NF:d2d1effecthelpers.ValueSetter
title: ValueSetter function
author: windows-sdk-content
description: Calls a member-function property setter callback for a value-type property.
old-location: direct2d\valuesetter.htm
old-project: Direct2D
ms.assetid: 5137D54E-1BAC-470C-AF16-0FB19DD36A61
ms.author: windowssdkdev
ms.date: 04/20/2018
ms.keywords: ValueSetter, ValueSetter function [Direct2D], d2d1effecthelpers/ValueSetter, direct2d.valuesetter
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
tech.root: 
req.typenames: D2D1_VERTEX_RANGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	d2d1.dll
api_name:
-	ValueSetter
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
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


### -param param

TBD




## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



