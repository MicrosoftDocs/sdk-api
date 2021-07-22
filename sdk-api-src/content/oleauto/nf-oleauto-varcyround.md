---
UID: NF:oleauto.VarCyRound
title: VarCyRound function (oleauto.h)
description: Rounds a variant of type currency to the specified number of decimal places.
helpviewer_keywords: ["VarCyRound","VarCyRound function [Automation]","_oa96_VarCyRound","automat.varcyround","oleauto/VarCyRound"]
old-location: automat\varcyround.htm
tech.root: automat
ms.assetid: d1292247-cf8a-46cc-94c9-858ec5d8cad7
ms.date: 12/05/2018
ms.keywords: VarCyRound, VarCyRound function [Automation], _oa96_VarCyRound, automat.varcyround, oleauto/VarCyRound
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VarCyRound
 - oleauto/VarCyRound
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - VarCyRound
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

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

