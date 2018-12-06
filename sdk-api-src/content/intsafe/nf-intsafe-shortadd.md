---
UID: NF:intsafe.ShortAdd
title: ShortAdd function
author: windows-sdk-content
description: Adds two values of type SHORT.
old-location: shell\ShortAdd.htm
tech.root: shell
ms.assetid: 8a26d824-6ed9-4f4f-8ee7-3616fec1bbc1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ShortAdd, ShortAdd function [Windows Shell], intsafe/ShortAdd, shell.ShortAdd
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
 - ShortAdd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ShortAdd function


## -description


Adds two values of type <b>SHORT</b>.


## -parameters




### -param sAugend [in]

The first value.


### -param sAddend [in]

The second value.


### -param psResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



