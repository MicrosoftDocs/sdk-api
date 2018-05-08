---
UID: NF:intsafe.ULongLongToULongPtr
title: ULongLongToULongPtr function
author: windows-driver-content
description: Converts a value of type ULONGLONG to a value of type DWORD_PTR.
old-location: shell\ULongLongToDWordPtr.htm
old-project: shell
ms.assetid: 7f398e08-44a1-4815-b49d-95259e502eba
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: ULongLongToDWordPtr, ULongLongToDWordPtr function [Windows Shell], ULongLongToULongPtr, _shell_ULongLongToDWordPtr, intsafe/ULongLongToDWordPtr, shell.ULongLongToDWordPtr
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
-	ULongLongToDWordPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ULongLongToULongPtr function


## -description


Converts a value of type <b>ULONGLONG</b> to a value of type <b>DWORD_PTR</b>.


## -parameters




### -param ullOperand [in]

Type: <b>ULONGLONG</b>

The value to be converted.


### -param pulResult

TBD




#### - pdwResult [out]

Type: <b>DWORD_PTR*</b>

The address of a pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



