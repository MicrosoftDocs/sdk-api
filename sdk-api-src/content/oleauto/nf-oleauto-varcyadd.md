---
UID: NF:oleauto.VarCyAdd
title: VarCyAdd function (oleauto.h)
description: Adds two variants of type currency.
helpviewer_keywords: ["VarCyAdd","VarCyAdd function [Automation]","_oa96_VarCyAdd","automat.varcyadd","oleauto/VarCyAdd"]
old-location: automat\varcyadd.htm
tech.root: automat
ms.assetid: ef0402aa-7263-4a4b-9204-a35d8da154c5
ms.date: 12/05/2018
ms.keywords: VarCyAdd, VarCyAdd function [Automation], _oa96_VarCyAdd, automat.varcyadd, oleauto/VarCyAdd
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
 - VarCyAdd
 - oleauto/VarCyAdd
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
 - VarCyAdd
---

# VarCyAdd function


## -description

Adds two variants of type currency.

## -parameters

### -param cyLeft [in]

The first variant.

### -param cyRight [in]

The second variant.

### -param pcyResult [out]

The resulting variant.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

