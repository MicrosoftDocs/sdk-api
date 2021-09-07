---
UID: NF:oleauto.VarCySub
title: VarCySub function (oleauto.h)
description: Subtracts two variants of type currency.
helpviewer_keywords: ["VarCySub","VarCySub function [Automation]","_oa96_VarCySub","automat.varcysub","oleauto/VarCySub"]
old-location: automat\varcysub.htm
tech.root: automat
ms.assetid: 248640b4-4c53-402b-af53-b76a809f0741
ms.date: 12/05/2018
ms.keywords: VarCySub, VarCySub function [Automation], _oa96_VarCySub, automat.varcysub, oleauto/VarCySub
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
 - VarCySub
 - oleauto/VarCySub
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
 - VarCySub
---

# VarCySub function


## -description

Subtracts two variants of type currency.

## -parameters

### -param cyLeft [in]

The first variant.

### -param cyRight [in]

The second variant.

### -param pcyResult [out]

The resulting variant.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

