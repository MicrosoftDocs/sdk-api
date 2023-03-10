---
UID: NF:oleauto.VarR8Round
title: VarR8Round function (oleauto.h)
description: Rounds a variant of type double to the specified number of decimal places.
helpviewer_keywords: ["VarR8Round","VarR8Round function [Automation]","_oa96_VarR8Round","automat.varr8round","oleauto/VarR8Round"]
old-location: automat\varr8round.htm
tech.root: automat
ms.assetid: bdf52cd6-a32d-4814-ac2f-51256dcc47cb
ms.date: 12/05/2018
ms.keywords: VarR8Round, VarR8Round function [Automation], _oa96_VarR8Round, automat.varr8round, oleauto/VarR8Round
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
 - VarR8Round
 - oleauto/VarR8Round
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
 - VarR8Round
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

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

