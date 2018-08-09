---
UID: NF:oleauto.VarRound
title: VarRound function
author: windows-sdk-content
description: Rounds a variant to the specified number of decimal places.
old-location: automat\varround.htm
old-project: automat
ms.assetid: 7713f477-f6a3-456d-a442-a78750542b03
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: VarRound, VarRound function [Automation], _oa96_VarRound, automat.varround, oleauto/VarRound
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: REGKIND
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarRound
product: Windows
targetos: Windows
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
req.product: ADAM
---

# VarRound function


## -description


Rounds a variant to the specified number of decimal places.


## -parameters




### -param pvarIn [in]

The variant.


### -param cDecimals [in]

The number of decimal places.


### -param pvarResult [out]

The result variant.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



