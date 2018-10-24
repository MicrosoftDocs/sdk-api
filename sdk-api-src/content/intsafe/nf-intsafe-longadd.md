---
UID: NF:intsafe.LongAdd
title: LongAdd function
author: windows-sdk-content
description: Adds two values of type LONG.
old-location: shell\LongAdd.htm
tech.root: shell
ms.assetid: 3cc13a46-3168-44fd-b759-06250eb1117f
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: LongAdd, LongAdd function [Windows Shell], intsafe/LongAdd, shell.LongAdd
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
 - LongAdd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LongAdd function


## -description


Adds two values of type <b>LONG</b>.


## -parameters




### -param lAugend [in]

The first value.


### -param lAddend [in]

The second value.


### -param plResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



