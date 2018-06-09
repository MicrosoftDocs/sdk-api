---
UID: NF:intsafe.LongLongToLong
title: LongLongToLong function
author: windows-sdk-content
description: Converts a value of type LONGLONG to a value of type LONG.
old-location: shell\LongLongToLong.htm
old-project: shell
ms.assetid: c77dbb9f-6c3a-4793-9740-ce9b75727b0d
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: Int64ToLong, LongLongToLong, LongLongToLong function [Windows Shell], intsafe/LongLongToLong, shell.LongLongToLong
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
tech.root: 
req.typenames: MANIPULATION_VELOCITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - LongLongToLong
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongLongToLong function


## -description


Converts a value of type <b>LONGLONG</b> to a value of type <b>LONG</b>.


## -parameters




### -param llOperand [in]

The value to convert.


### -param plResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Int64ToLong</b> is an alias for this function.



