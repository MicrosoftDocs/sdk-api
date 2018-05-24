---
UID: NF:oleauto.VarR8Round
title: VarR8Round function
author: windows-driver-content
description: Rounds a variant of type double to the specified number of decimal places.
old-location: automat\varr8round.htm
old-project: automat
ms.assetid: bdf52cd6-a32d-4814-ac2f-51256dcc47cb
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: VarR8Round, VarR8Round function [Automation], _oa96_VarR8Round, automat.varr8round, oleauto/VarR8Round
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
-	VarR8Round
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# VarR8Round function


## -description


Rounds a variant of type double to the specified number of decimal places.


## -parameters




### -param dblIn [in]

The variant.


### -param cDecimals [in]

The number of decimal places.



### -param pdblResult [out]

The result.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



