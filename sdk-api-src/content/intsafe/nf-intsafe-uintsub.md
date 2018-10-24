---
UID: NF:intsafe.UIntSub
title: UIntSub function
author: windows-sdk-content
description: Subtracts one value of type UINT from another.
old-location: shell\UIntSub.htm
tech.root: shell
ms.assetid: be257075-84c9-40e2-af3f-75dccd97bab1
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: UIntSub, UIntSub function [Windows Shell], _shell_UIntSub, intsafe/UIntSub, shell.UIntSub
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Intsafe.h
api_name:
 - UIntSub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UIntSub function


## -description


Subtracts one value of type <b>UINT</b> from another.


## -parameters




### -param uMinuend [in]

Type: <b>UINT</b>

The value from which <i>uSubtrahend</i> is subtracted.


### -param uSubtrahend [in]

Type: <b>UINT</b>

The value to subtract from <i>uMinuend</i>.


### -param puResult [out]

Type: <b>UINT*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



