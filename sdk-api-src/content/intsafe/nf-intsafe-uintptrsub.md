---
UID: NF:intsafe.UIntPtrSub
title: UIntPtrSub function
author: windows-sdk-content
description: Subtracts one value of type UINT_PTR from another.
old-location: shell\UIntPtrSub.htm
old-project: shell
ms.assetid: 629bc700-ca64-4849-bdad-59e67857ff8d
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: UIntPtrSub, UIntPtrSub function [Windows Shell], _shell_UIntPtrSub, intsafe/UIntPtrSub, shell.UIntPtrSub
ms.prod: windows
ms.technology: windows-sdk
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
-	UIntPtrSub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrSub function


## -description


Subtracts one value of type <b>UINT_PTR</b> from another.


## -parameters




### -param uMinuend [in]

Type: <b>UINT_PTR</b>

The value from which <i>uSubtrahend</i> is subtracted.


### -param uSubtrahend [in]

Type: <b>UINT_PTR</b>

The value to subtract from <i>uMinuend</i>.


### -param puResult [out]

Type: <b>UINT_PTR*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



