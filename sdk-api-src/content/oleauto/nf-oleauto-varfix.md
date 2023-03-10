---
UID: NF:oleauto.VarFix
title: VarFix function (oleauto.h)
description: Returns the integer portion of a variant. (VarFix)
helpviewer_keywords: ["VarFix","VarFix function [Automation]","_oa96_VarFix","automat.varfix","oleauto/VarFix"]
old-location: automat\varfix.htm
tech.root: automat
ms.assetid: d90f37c7-87a8-4800-901c-d2aa3e5d838b
ms.date: 12/05/2018
ms.keywords: VarFix, VarFix function [Automation], _oa96_VarFix, automat.varfix, oleauto/VarFix
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
 - VarFix
 - oleauto/VarFix
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
 - VarFix
---

# VarFix function


## -description

Returns the integer portion of a variant.

## -parameters

### -param pvarIn [in]

The variant.

### -param pvarResult [out]

The result variant.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If the variant is negative, then the first negative integer greater than or equal to the variant is returned.

