---
UID: NF:intsafe.SizeTMult
title: SizeTMult function
author: windows-sdk-content
description: Multiplies one value of type size_t by another.
old-location: shell\SizeTMult.htm
old-project: shell
ms.assetid: 078bc77b-6af3-4d13-8f98-5f52605fdf8d
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: SizeTMult, SizeTMult function [Windows Shell], ULongLongMult, _shell_SizeTMult, intsafe/SizeTMult, shell.SizeTMult
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
 - SizeTMult
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# SizeTMult function


## -description


Multiplies one value of type <b>size_t</b> by another.


## -parameters




### -param Multiplicand

TBD


### -param Multiplier

TBD


### -param pResult

TBD




#### - cbMultiplicand [in]

Type: <b>size_t</b>

The value to be multiplied by <i>cbMultiplier</i>.


#### - cbMultiplier [in]

Type: <b>size_t</b>

The value by which to multiply <i>cbMultiplicand</i>.


#### - pcbResult [out]

Type: <b>size_t*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



