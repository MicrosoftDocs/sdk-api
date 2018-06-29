---
UID: NF:intsafe.SizeTAdd
title: SizeTAdd function
author: windows-sdk-content
description: Adds two values of type size_t.
old-location: shell\SizeTAdd.htm
old-project: shell
ms.assetid: 1cabc944-0819-4a24-ab61-6d5375ba1573
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: SizeTAdd, SizeTAdd function [Windows Shell], _shell_SizeTAdd, intsafe/SizeTAdd, shell.SizeTAdd
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
 - SizeTAdd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# SizeTAdd function


## -description


Adds two values of type <b>size_t</b>.


## -parameters




### -param Augend

TBD


### -param Addend

TBD


### -param pResult

TBD




#### - cbAddend [in]

Type: <b>size_t</b>

The value to add to <i>cbAugend</i>.


#### - cbAugend [in]

Type: <b>size_t</b>

The first value in the equation.


#### - pcbResult [out]

Type: <b>size_t*</b>

A pointer to the sum. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



