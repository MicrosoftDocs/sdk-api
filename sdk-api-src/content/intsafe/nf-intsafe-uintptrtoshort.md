---
UID: NF:intsafe.UIntPtrToShort
title: UIntPtrToShort function
author: windows-sdk-content
description: Converts a value of type UINT_PTR to a value of type SHORT.
old-location: shell\UIntPtrToShort.htm
tech.root: shell
ms.assetid: 6cbbced2-5a0f-49d6-8ac0-27a9d1a885fe
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: UIntPtrToShort, UIntPtrToShort function [Windows Shell], intsafe/UIntPtrToShort, shell.UIntPtrToShort
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - UIntPtrToShort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UIntPtrToShort function


## -description


Converts a value of type <b>UINT_PTR</b> to a value of type <b>SHORT</b>.


## -parameters




### -param uOperand [in]

The value to convert.


### -param psResult [out]

The converted value.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



