---
UID: NF:intsafe.UIntAdd
title: UIntAdd function
author: windows-driver-content
description: Adds two values of type UINT.
old-location: shell\UIntAdd.htm
old-project: shell
ms.assetid: 387d53e8-3e52-470f-bfd2-ad2b1e0a3d5a
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: UIntAdd, UIntAdd function [Windows Shell], _shell_UIntAdd, intsafe/UIntAdd, shell.UIntAdd
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: intsafe.h
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
req.typenames: MANIPULATION_VELOCITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Intsafe.h
api_name:
-	UIntAdd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntAdd function


## -description


Adds two values of type <b>UINT</b>.


## -parameters




### -param uAugend [in]

Type: <b>UINT</b>

The first value in the equation.


### -param uAddend [in]

Type: <b>UINT</b>

The value to add to <i>uAugend</i>.


### -param puResult [out]

Type: <b>UINT*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



