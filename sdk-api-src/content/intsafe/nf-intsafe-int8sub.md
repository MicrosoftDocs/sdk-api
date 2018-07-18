---
UID: NF:intsafe.Int8Sub
title: Int8Sub function
author: windows-sdk-content
description: Subtracts one value of type INT8 from another.
old-location: shell\Int8Sub.htm
old-project: shell
ms.assetid: 2dfab719-3c16-49db-9cf3-1db236eae141
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: Int8Sub, Int8Sub function [Windows Shell], intsafe/Int8Sub, shell.Int8Sub
ms.prod: windows
ms.technology: windows-sdk
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
 - Int8Sub
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Int8Sub function


## -description


Subtracts one value of type <b>INT8</b> from another.


## -parameters




### -param i8Minuend [in]

The first value.


### -param i8Subtrahend [in]

The value to subtract.


### -param pi8Result [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



