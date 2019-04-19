---
UID: NF:intsafe.ULongPtrToShort
title: ULongPtrToShort function (intsafe.h)
author: windows-sdk-content
description: Converts a value of type ULONG_PTR to a value of type SHORT.
old-location: shell\ULongPtrToShort.htm
tech.root: shell
ms.assetid: cb3d598b-24c4-45b0-838e-de41ac69f691
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ULongPtrToShort, ULongPtrToShort function [Windows Shell], intsafe/ULongPtrToShort, shell.ULongPtrToShort
ms.topic: function
req.header: intsafe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - intsafe.h
api_name:
 - ULongPtrToShort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ULongPtrToShort function


## -description


Converts a value of type <b>ULONG_PTR</b> to a value of type <b>SHORT</b>.


## -parameters




### -param ulOperand [in]

The value to convert.


### -param psResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



