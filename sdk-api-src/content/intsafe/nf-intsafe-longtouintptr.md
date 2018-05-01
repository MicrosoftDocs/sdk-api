---
UID: NF:intsafe.LongToUIntPtr
title: LongToUIntPtr function
author: windows-driver-content
description: Converts a value of type LONG to a value of type size_t.
old-location: shell\LongToSizeT.htm
old-project: shell
ms.assetid: 77a3e14f-1dc9-42f6-9ff1-579c5223932d
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: LongToSizeT, LongToSizeT function [Windows Shell], LongToUIntPtr, _shell_LongToSizeT, intsafe/LongToSizeT, shell.LongToSizeT
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
-	LongToSizeT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongToUIntPtr function


## -description


Converts a value of type <b>LONG</b> to a value of type <b>size_t</b>.


## -parameters




### -param lOperand [in]

Type: <b>LONG</b>

The value to be converted.


### -param puResult

TBD




#### - pcbResult [out]

Type: <b>size_t*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



