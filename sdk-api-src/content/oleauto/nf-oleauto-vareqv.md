---
UID: NF:oleauto.VarEqv
title: VarEqv function (oleauto.h)
description: Performs a bitwise equivalence on two variants.
helpviewer_keywords: ["VarEqv","VarEqv function [Automation]","_oa96_VarEqv","automat.vareqv","oleauto/VarEqv"]
old-location: automat\vareqv.htm
tech.root: automat
ms.assetid: 34ddece6-87c8-469d-b275-443d1e99b1c9
ms.date: 12/05/2018
ms.keywords: VarEqv, VarEqv function [Automation], _oa96_VarEqv, automat.vareqv, oleauto/VarEqv
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
 - VarEqv
 - oleauto/VarEqv
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
 - VarEqv
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

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If each bit in <i>pvarLeft</i> is equal to the corresponding bit in <i>pvarRight</i> then TRUE is returned. Otherwise FALSE is returned.

