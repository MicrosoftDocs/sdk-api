---
UID: NF:oleauto.VarCyRound
title: VarCyRound function
author: windows-driver-content
description: Rounds a variant of type currency to the specified number of decimal places.
old-location: automat\varcyround.htm
old-project: automat
ms.assetid: d1292247-cf8a-46cc-94c9-858ec5d8cad7
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: VarCyRound, VarCyRound function [Automation], _oa96_VarCyRound, automat.varcyround, oleauto/VarCyRound
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
-	VarCyRound
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VarCyRound function


## -description


Rounds a variant of type currency to the specified number of decimal places.


## -parameters




### -param cyIn [in]

The variant to round.


### -param cDecimals [in]

The number of currency decimals.


### -param pcyResult [out]

The resulting variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



