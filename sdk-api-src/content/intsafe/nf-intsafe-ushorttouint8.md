---
UID: NF:intsafe.UShortToUInt8
title: UShortToUInt8 function (intsafe.h)
description: Converts a value of type USHORT to a value of type UINT8.
helpviewer_keywords: ["UShortToByte","UShortToUInt8","UShortToUInt8 function [Windows Shell]","WordToByte","intsafe/UShortToUInt8","shell.UShortToUInt8"]
old-location: shell\UShortToUInt8.htm
tech.root: shell
ms.assetid: 86e8a064-ce83-4224-81d3-84db39905f34
ms.date: 12/05/2018
ms.keywords: UShortToByte, UShortToUInt8, UShortToUInt8 function [Windows Shell], WordToByte, intsafe/UShortToUInt8, shell.UShortToUInt8
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UShortToUInt8
 - intsafe/UShortToUInt8
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - UShortToUInt8
---

# UShortToUInt8 function


## -description

Converts a value of type <b>USHORT</b> to a value of type <b>UINT8</b>.

## -parameters

### -param usOperand [in]

The value to convert.

### -param pui8Result [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>WordToByte</b> is an alias for this function.

<b>UShortToByte</b> is an alias for this function.

