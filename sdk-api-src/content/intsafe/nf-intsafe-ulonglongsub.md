---
UID: NF:intsafe.ULongLongSub
title: ULongLongSub function
author: windows-driver-content
description: Subtracts one value of type ULONGLONG from another.
old-location: shell\ULongLongSub.htm
old-project: shell
ms.assetid: bffec47c-6985-42e7-b7df-c0cd1f090e0c
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ULongLongSub, ULongLongSub function [Windows Shell], _shell_ULongLongSub, intsafe/ULongLongSub, shell.ULongLongSub
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
-	ULongLongSub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongLongSub function


## -description


Subtracts one value of type <b>ULONGLONG</b> from another.


## -parameters




### -param ullMinuend [in]

Type: <b>ULONGLONG</b>

The value from which <i>ullSubtrahend</i> is subtracted.


### -param ullSubtrahend [in]

Type: <b>ULONGLONG</b>

The value to subtract from <i>ullMinuend</i>.


### -param pullResult [out]

Type: <b>ULONGLONG*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



