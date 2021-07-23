---
UID: NF:oleauto.VarDecRound
title: VarDecRound function (oleauto.h)
description: Rounds a variant of type decimal to the specified number of decimal places.
helpviewer_keywords: ["VarDecRound","VarDecRound function [Automation]","_oa96_VarDecRound","automat.vardecround","oleauto/VarDecRound"]
old-location: automat\vardecround.htm
tech.root: automat
ms.assetid: 264914c6-2f47-4e99-b3bb-a2c510906954
ms.date: 12/05/2018
ms.keywords: VarDecRound, VarDecRound function [Automation], _oa96_VarDecRound, automat.vardecround, oleauto/VarDecRound
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
 - VarDecRound
 - oleauto/VarDecRound
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
 - VarDecRound
---

# VarDecRound function


## -description

Rounds a variant of type decimal to the specified number of decimal places.

## -parameters

### -param pdecIn [in]

The variant to round.

### -param cDecimals [in]

The number of decimal places.

### -param pdecResult [out]

The resulting variant.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

