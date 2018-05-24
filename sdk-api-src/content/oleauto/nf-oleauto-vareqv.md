---
UID: NF:oleauto.VarEqv
title: VarEqv function
author: windows-driver-content
description: Performs a bitwise equivalence on two variants.
old-location: automat\vareqv.htm
old-project: automat
ms.assetid: 34ddece6-87c8-469d-b275-443d1e99b1c9
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: VarEqv, VarEqv function [Automation], _oa96_VarEqv, automat.vareqv, oleauto/VarEqv
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: REGKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	OleAut32.dll
api_name:
-	VarEqv
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VarEqv function


## -description


Performs a bitwise equivalence on two variants.


## -parameters




### -param pvarLeft [in]

The first variant.


### -param pvarRight [in]

The second variant.


### -param pvarResult [out]

The result variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If each bit in <i>pvarLeft</i> is equal to the corresponding bit in <i>pvarRight</i> then TRUE is returned. Otherwise FALSE is returned.



