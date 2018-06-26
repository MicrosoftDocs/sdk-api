---
UID: NF:intsafe.UIntPtrToLongLong
title: UIntPtrToLongLong function
author: windows-sdk-content
description: Converts a value of type UINT_PTR to a value of type LONGLONG.
old-location: shell\UIntPtrToLongLong.htm
old-project: shell
ms.assetid: 95d9153c-e9bd-4098-ad5f-2128ebed8140
ms.author: windowssdkdev
ms.date: 06/11/2018
ms.keywords: SizeTToInt64, UIntPtrToLongLong, UIntPtrToLongLong function [Windows Shell], intsafe/UIntPtrToLongLong, shell.UIntPtrToLongLong
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
 - UIntPtrToLongLong
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# UIntPtrToLongLong function


## -description


Converts a value of type <b>UINT_PTR</b> to a value of type <b>LONGLONG</b>.


## -parameters




### -param uOperand [in]

The value to convert.


### -param pllResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>SizeTToInt64</b> is an alias for this function.



