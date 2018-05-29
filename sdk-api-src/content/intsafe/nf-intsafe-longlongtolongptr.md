---
UID: NF:intsafe.LongLongToLongPtr
title: LongLongToLongPtr function
author: windows-sdk-content
description: Converts a value of type LONGLONG to a value of type LONG_PTR.
old-location: shell\LongLongToLongPtr.htm
old-project: shell
ms.assetid: adda2fcd-2589-4506-a147-b2d32d7fbd69
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: Int64ToLongPtr, Int64ToSSIZET, Int64ToULongPtr, LongLongToLongPtr, LongLongToLongPtr function [Windows Shell], intsafe/LongLongToLongPtr, shell.LongLongToLongPtr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
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
-	intsafe.h
api_name:
-	LongLongToLongPtr
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToLongPtr function


## -description


Converts a value of type <b>LONGLONG</b> to a value of type <b>LONG_PTR</b>.


## -parameters




### -param llOperand [in]

The value to convert.


### -param plResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Int64ToSSIZET</b> is an alias for this function.

<b>Int64ToULongPtr</b> is an alias for this function.

<b>Int64ToLongPtr</b> is an alias for this function.



