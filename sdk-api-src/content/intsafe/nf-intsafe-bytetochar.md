---
UID: NF:intsafe.ByteToChar
title: ByteToChar function (intsafe.h)
description: Converts a value of type BYTE to a value of type CHAR.
helpviewer_keywords: ["ByteToChar","ByteToChar function [Windows Shell]","intsafe/ByteToChar","shell.ByteToChar"]
old-location: shell\ByteToChar.htm
tech.root: shell
ms.assetid: d10b3450-3dfc-4acf-9853-f7c191041b33
ms.date: 12/05/2018
ms.keywords: ByteToChar, ByteToChar function [Windows Shell], intsafe/ByteToChar, shell.ByteToChar
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
 - ByteToChar
 - intsafe/ByteToChar
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
 - ByteToChar
---

# ByteToChar function


## -description

Converts a value of type <b>BYTE</b> to a value of type <b>CHAR</b>.

## -parameters

### -param bOperand [in]

The value to convert.

### -param pch [out]

The converted value.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

