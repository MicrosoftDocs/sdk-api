---
UID: NF:oleauto.VarMod
title: VarMod function (oleauto.h)
description: Divides two variants and returns only the remainder.
helpviewer_keywords: ["VarMod","VarMod function [Automation]","_oa96_VarMod","automat.varmod","oleauto/VarMod"]
old-location: automat\varmod.htm
tech.root: automat
ms.assetid: 910d3f37-15f4-4a0e-8aa0-ab58be865c62
ms.date: 12/05/2018
ms.keywords: VarMod, VarMod function [Automation], _oa96_VarMod, automat.varmod, oleauto/VarMod
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
 - VarMod
 - oleauto/VarMod
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
 - VarMod
---

# VarMod function


## -description

Divides two variants and returns only the remainder.

## -parameters

### -param pvarLeft [in]

The first variant.

### -param pvarRight [in]

The second variant.

### -param pvarResult [out]

The result variant.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

