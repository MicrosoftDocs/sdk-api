---
UID: NF:intsafe.DWordPtrSub
title: DWordPtrSub function
author: windows-sdk-content
description: Subtracts one value of type DWORD_PTR from another.
old-location: shell\DWordPtrSub.htm
tech.root: shell
ms.assetid: cfe9ec32-ed6a-42fa-9891-3ce2e88cd5d0
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DWordPtrSub, DWordPtrSub function [Windows Shell], _shell_DWordPtrSub, intsafe/DWordPtrSub, shell.DWordPtrSub
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
req.dll: None
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - None
api_name:
 - DWordPtrSub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DWordPtrSub
: 
---

# DWordPtrSub function


## -description


Subtracts one value of type <b>DWORD_PTR</b> from another.


## -parameters




### -param dwMinuend [in]

Type: <b>DWORD_PTR</b>

The value from which <i>dwSubtrahend</i> is subtracted.


### -param dwSubtrahend [in]

Type: <b>DWORD_PTR</b>

The value to subtract from <i>dwMinuend</i>.


### -param pdwResult [out]

Type: <b>DWORD_PTR*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



