---
UID: NF:intsafe.ULongSub
title: ULongSub function
author: windows-driver-content
description: Subtracts one value of type DWORD from another.
old-location: shell\DWordSub.htm
old-project: shell
ms.assetid: 327bd93f-be3c-4a3c-8aca-4250cf9c88c3
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: DWordSub, DWordSub function [Windows Shell], ULongSub, _shell_DWordSub, intsafe/DWordSub, shell.DWordSub
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
-	DllExport
api_location:
-	None
api_name:
-	DWordSub
product: Windows
targetos: Windows
req.lib: 
req.dll: None
req.irql: 
req.product: GDI+ 1.1
---

# ULongSub function


## -description


Subtracts one value of type <b>DWORD</b> from another.


## -parameters




### -param ulMinuend

TBD


### -param ulSubtrahend

TBD


### -param pulResult

TBD




#### - dwMinuend [in]

Type: <b>DWORD</b>

The value from which <i>dwSubtrahend</i> is subtracted.


#### - dwSubtrahend [in]

Type: <b>DWORD</b>

The value to subtract from <i>dwMinuend</i>.


#### - pdwResult [out]

Type: <b>DWORD*</b>

A pointer to the result. If the operation results in a value that overflows or underflows the capacity of the type, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide arithmetic operations and perform validity checks with minimal impact on performance.



