---
UID: NF:intsafe.UIntPtrToUChar
title: UIntPtrToUChar function (intsafe.h)

description: Converts a value of type UINT_PTR to a value of type UCHAR.
old-location: shell\UIntPtrToUChar.htm
tech.root: shell
ms.assetid: b69f2f7b-4f93-40f4-aaea-1b606e694680

ms.date: 12/05/2018
ms.keywords: UIntPtrToUChar, UIntPtrToUChar function [Windows Shell], intsafe/UIntPtrToUChar, shell.UIntPtrToUChar
ms.topic: function
f1_keywords: 
 - "intsafe/UIntPtrToUChar"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - UIntPtrToUChar
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UIntPtrToUChar function


## -description


Converts a value of type <b>UINT_PTR</b> to a value of type <b>UCHAR</b>.


## -parameters




### -param uOperand [in]

The value to convert.


### -param pch [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



