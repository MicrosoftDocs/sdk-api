---
UID: NF:oleauto.VarRound
title: VarRound function (oleauto.h)
description: Rounds a variant to the specified number of decimal places.
helpviewer_keywords: ["VarRound","VarRound function [Automation]","_oa96_VarRound","automat.varround","oleauto/VarRound"]
old-location: automat\varround.htm
tech.root: automat
ms.assetid: 7713f477-f6a3-456d-a442-a78750542b03
ms.date: 12/05/2018
ms.keywords: VarRound, VarRound function [Automation], _oa96_VarRound, automat.varround, oleauto/VarRound
f1_keywords:
- oleauto/VarRound
dev_langs:
- c++
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- OleAut32.dll
api_name:
- VarRound
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



