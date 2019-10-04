---
UID: NF:intsafe.LongLongMult
title: LongLongMult function (intsafe.h)
author: windows-sdk-content
description: Multiplies two values of type LONGLONG.
old-location: shell\LongLongMult.htm
tech.root: shell
ms.assetid: 71f9cef9-33a2-48f2-a14f-aad364116e93
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LongLongMult, LongLongMult function [Windows Shell], intsafe/LongLongMult, shell.LongLongMult
ms.topic: function
f1_keywords: 
 - "intsafe/LongLongMult"
dev_langs:
 - c++
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
 - LongLongMult
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LongLongMult function


## -description


Multiplies two values of type <b>LONGLONG</b>.


## -parameters




### -param llMultiplicand [in]

The first value.


### -param llMultiplier [in]

The second value.


### -param pllResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



