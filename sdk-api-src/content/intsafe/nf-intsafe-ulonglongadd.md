---
UID: NF:intsafe.ULongLongAdd
title: ULongLongAdd function
author: windows-sdk-content
description: Adds two values of type SIZE_T.
old-location: shell\SIZETAdd_1.htm
tech.root: shell
ms.assetid: 50acd1fa-fc4b-4e7a-8e88-71fb15eaa3c7
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: SIZETAdd, SIZETAdd function [Windows Shell], ULongLongAdd, _shell_SIZETAdd, intsafe/SIZETAdd, shell.SIZETAdd, shell.SIZETAdd_1
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
 - SIZETAdd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ULongLongAdd function


## -description


Adds two values of type <b>SIZE_T</b>.


## -parameters




### -param ullAugend [in]

Type: <b>SIZE_T</b>

The first value in the equation.


### -param ullAddend [in]

Type: <b>SIZE_T</b>

The value to add to <i>cbAugend</i>.


### -param pullResult [out]

Type: <b>SIZE_T*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



