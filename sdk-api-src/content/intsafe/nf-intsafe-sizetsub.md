---
UID: NF:intsafe.SizeTSub
title: SizeTSub function
author: windows-sdk-content
description: Subtracts one value of type size_t from another.
old-location: shell\SizeTSub.htm
old-project: shell
ms.assetid: 6a7b22e7-504b-4065-80fa-b972f0360b5c
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: SizeTSub, SizeTSub function [Windows Shell], _shell_SizeTSub, intsafe/SizeTSub, shell.SizeTSub
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
 - SizeTSub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# SizeTSub function


## -description


Subtracts one value of type <b>size_t</b> from another.


## -parameters




### -param Minuend

TBD


### -param Subtrahend

TBD


### -param pResult

TBD




#### - cbMinuend [in]

Type: <b>size_t</b>

The value from which <i>cbSubtrahend</i> is subtracted.


#### - cbSubtrahend [in]

Type: <b>size_t</b>

The value to subtract from <i>cbMinuend</i>.


#### - pcbResult [out]

Type: <b>size_t*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



