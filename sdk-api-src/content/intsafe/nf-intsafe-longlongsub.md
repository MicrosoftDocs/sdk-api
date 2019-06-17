---
UID: NF:intsafe.LongLongSub
title: LongLongSub function (intsafe.h)
author: windows-sdk-content
description: Subtracts one value of type LONGLONG from another.
old-location: shell\LongLongSub.htm
tech.root: shell
ms.assetid: 8c6c65c7-0f93-4823-a6f3-cc59c4b5b207
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: LongLongSub, LongLongSub function [Windows Shell], intsafe/LongLongSub, shell.LongLongSub
ms.topic: function
f1_keywords: ["intsafe/LongLongSub"]
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
 - LongLongSub
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# LongLongSub function


## -description


Subtracts one value of type <b>LONGLONG</b> from another.


## -parameters




### -param llMinuend [in]

The first value.


### -param llSubtrahend [in]

The value to subtract.


### -param pllResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



