---
UID: NF:intsafe.IntAdd
title: IntAdd function
author: windows-sdk-content
description: Adds two values of type INT.
old-location: shell\IntAdd.htm
tech.root: shell
ms.assetid: 0ae27240-2923-4caf-955a-0b10bd9e2515
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: IntAdd, IntAdd function [Windows Shell], intsafe/IntAdd, shell.IntAdd
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
 - IntAdd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IntAdd function


## -description


Adds two values of type <b>INT</b>.


## -parameters




### -param iAugend [in]

The first value.


### -param iAddend [in]

The second value.


### -param piResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



