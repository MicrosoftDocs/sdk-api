---
UID: NF:oleauto.DispCallFunc
title: DispCallFunc function (oleauto.h)
description: Low-level helper for Invoke that provides machine independence for customized Invoke. (DispCallFunc)
helpviewer_keywords: ["DispCallFunc","DispCallFunc function [Automation]","_oa96_DispCallFunc","automat.dispcallfunc","oleauto/DispCallFunc"]
old-location: automat\dispcallfunc.htm
tech.root: automat
ms.assetid: 9a16d4e4-a03d-459d-a2ec-3258499f6932
ms.date: 12/05/2018
ms.keywords: DispCallFunc, DispCallFunc function [Automation], _oa96_DispCallFunc, automat.dispcallfunc, oleauto/DispCallFunc
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
 - DispCallFunc
 - oleauto/DispCallFunc
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
 - DispCallFunc
---

# DispCallFunc function


## -description

Low-level helper for <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a> that provides machine independence for customized <b>Invoke</b>.

## -parameters

### -param pvInstance

An instance of the interface described by this type description.

### -param oVft

For FUNC_VIRTUAL functions, specifies the offset in the VTBL.

### -param cc

The calling convention. One of the CALLCONV values, such as CC_STDCALL.

### -param vtReturn

The variant type of the function return value. Use VT_EMPTY to represent void.

### -param cActuals

The number of function parameters.

### -param prgvt

An array of variant types of the function parameters.

### -param prgpvarg

The function parameters.

### -param pvargResult

The function result.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.
