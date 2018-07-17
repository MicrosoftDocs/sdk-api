---
UID: NF:intsafe.LongPtrToShort
title: LongPtrToShort function
author: windows-sdk-content
description: Converts a value of type LONG_PTR to a value of type SHORT.
old-location: shell\LongPtrToShort.htm
old-project: shell
ms.assetid: db3236c4-0eac-4484-b36c-fcfa3e148b42
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: LongPtrToShort, LongPtrToShort function [Windows Shell], intsafe/LongPtrToShort, shell.LongPtrToShort
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
 - LongPtrToShort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# LongPtrToShort function


## -description


Converts a value of type <b>LONG_PTR</b> to a value of type <b>SHORT</b>.


## -parameters




### -param lOperand [in]

The value to convert.


### -param psResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



