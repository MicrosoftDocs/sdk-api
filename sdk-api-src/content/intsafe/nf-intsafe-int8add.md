---
UID: NF:intsafe.Int8Add
title: Int8Add function
author: windows-driver-content
description: Adds two values of type INT8.
old-location: shell\Int8Add.htm
old-project: shell
ms.assetid: 2b9e9c0b-ddf4-4a95-a743-004a7575bbfa
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Int8Add, Int8Add function [Windows Shell], intsafe/Int8Add, shell.Int8Add
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MANIPULATION_VELOCITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	intsafe.h
api_name:
-	Int8Add
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# Int8Add function


## -description


Adds two values of type <b>INT8</b>.


## -parameters




### -param i8Augend [in]

The first value.


### -param i8Addend [in]

The second value.


### -param pi8Result [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



