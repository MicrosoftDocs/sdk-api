---
UID: NF:oleauto.VarBstrCat
title: VarBstrCat function (oleauto.h)
description: Concatenates two variants of type BSTR and returns the resulting BSTR.
helpviewer_keywords: ["VarBstrCat","VarBstrCat function [Automation]","_oa96_VarBstrCat","automat.varbstrcat","oleauto/VarBstrCat"]
old-location: automat\varbstrcat.htm
tech.root: automat
ms.assetid: e23e1130-dd95-43ec-8ea3-c213fd6b0b25
ms.date: 12/05/2018
ms.keywords: VarBstrCat, VarBstrCat function [Automation], _oa96_VarBstrCat, automat.varbstrcat, oleauto/VarBstrCat
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
 - VarBstrCat
 - oleauto/VarBstrCat
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
 - VarBstrCat
---

# VarBstrCat function


## -description

Concatenates two variants of type BSTR and returns the resulting BSTR.

## -parameters

### -param bstrLeft [in]

The first variant.

### -param bstrRight [in]

The second variant.

### -param pbstrResult [out]

The result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

