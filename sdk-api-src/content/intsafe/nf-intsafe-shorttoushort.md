---
UID: NF:intsafe.ShortToUShort
title: ShortToUShort function
author: windows-driver-content
description: Converts a value of type SHORT to a value of type USHORT.
old-location: shell\ShortToUShort.htm
old-project: shell
ms.assetid: 35820e7f-db32-439b-a96b-8891ab2ab5ae
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: ShortToUShort, ShortToUShort function [Windows Shell], _shell_ShortToUShort, intsafe/ShortToUShort, shell.ShortToUShort
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
-	ShortToUShort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# ShortToUShort function


## -description


Converts a value of type <b>SHORT</b> to a value of type <b>USHORT</b>.


## -parameters




### -param sOperand [in]

Type: <b>SHORT</b>

The value to be converted.


### -param pusResult [out]

Type: <b>USHORT*</b>

A pointer to the converted value. In the case where the conversion causes a truncation of the original value, the function returns INTSAFE_E_ARITHMETIC_OVERFLOW and this parameter is not valid.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This is one of a set of inline functions designed to provide type conversions and perform validity checks with minimal impact on performance.



