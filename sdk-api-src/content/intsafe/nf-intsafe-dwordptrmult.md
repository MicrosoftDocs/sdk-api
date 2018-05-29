---
UID: NF:intsafe.DWordPtrMult
title: DWordPtrMult function
author: windows-sdk-content
description: Multiplies one value of type DWORD_PTR by another.
old-location: shell\DWordPtrMult.htm
old-project: shell
ms.assetid: 9f5beb13-17cd-44ef-a352-843d51304ab6
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DWordPtrMult, DWordPtrMult function [Windows Shell], _shell_DWordPtrMult, intsafe/DWordPtrMult, shell.DWordPtrMult
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
-	DllExport
api_location:
-	None
api_name:
-	DWordPtrMult
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# DWordPtrMult function


## -description


Multiplies one value of type <b>DWORD_PTR</b> by another.


## -parameters




### -param dwMultiplicand [in]

Type: <b>DWORD_PTR</b>

The value to be multiplied by <i>dwMultiplier</i>.


### -param dwMultiplier [in]

Type: <b>DWORD_PTR</b>

The value by which to multiply <i>dwMultiplicand</i>.


### -param pdwResult [out]

Type: <b>DWORD_PTR*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



