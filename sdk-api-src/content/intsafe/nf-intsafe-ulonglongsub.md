---
UID: NF:intsafe.ULongLongSub
title: ULongLongSub function
author: windows-sdk-content
description: Subtracts one value of type SIZE_T from another.
old-location: shell\SIZETSub_1.htm
old-project: shell
ms.assetid: 10c66f6a-648d-4308-9c23-384ebe273af3
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: SIZETSub, SIZETSub function [Windows Shell], ULongLongSub, _shell_SIZETSub, intsafe/SIZETSub, shell.SIZETSub, shell.SIZETSub_1
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
tech.root: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intsafe.h
api_name:
 - SIZETSub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongLongSub function


## -description


Subtracts one value of type <b>SIZE_T</b> from another.


## -parameters




### -param ullMinuend

TBD


### -param ullSubtrahend

TBD


### -param pullResult

TBD




#### - cbMinuend [in]

Type: <b>SIZE_T</b>

The value from which <i>cbSubtrahend</i> is subtracted.


#### - cbSubtrahend [in]

Type: <b>SIZE_T</b>

The value to subtract from <i>cbMinuend</i>.


#### - pcbResult [out]

Type: <b>SIZE_T*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



