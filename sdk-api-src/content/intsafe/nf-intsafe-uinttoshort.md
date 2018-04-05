---
UID: NF:intsafe.UIntToShort
title: UIntToShort function
author: windows-driver-content
description: Converts a value of type UINT to a value of type SHORT.
old-location: shell\UIntToShort.htm
old-project: shell
ms.assetid: abad8095-ac1b-4604-b423-5b244fa60127
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: UIntToShort, UIntToShort function [Windows Shell], _shell_UIntToShort, intsafe/UIntToShort, shell.UIntToShort
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
-	UIntToShort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntToShort function


## -description


Converts a value of type <b>UINT</b> to a value of type <b>SHORT</b>.


## -parameters




### -param uOperand [in]

Type: <b>UINT</b>

The value to be converted.


### -param psResult [out]

Type: <b>SHORT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



