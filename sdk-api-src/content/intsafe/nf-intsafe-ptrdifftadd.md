---
UID: NF:intsafe.PtrdiffTAdd
title: PtrdiffTAdd function
author: windows-driver-content
description: Adds two values of type ptrdiff_t.
old-location: shell\PtrdiffTAdd.htm
old-project: shell
ms.assetid: ed670d8a-ede5-47c5-9cf9-eea32609f195
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: PtrdiffTAdd, PtrdiffTAdd function [Windows Shell], intsafe/PtrdiffTAdd, shell.PtrdiffTAdd
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
-	PtrdiffTAdd
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# PtrdiffTAdd function


## -description


Adds two values of type <b>ptrdiff_t</b>.


## -parameters




### -param Augend [in]

The first value.


### -param Addend [in]

The second value.


### -param pResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



