---
UID: NF:dcomp.IDCompositionDevice3.CreateTurbulenceEffect
title: IDCompositionDevice3::CreateTurbulenceEffect (dcomp.h)
description: Creates an instance of IDCompositionTurbulenceEffect.
helpviewer_keywords: ["CreateTurbulenceEffect","CreateTurbulenceEffect method [DirectComposition]","CreateTurbulenceEffect method [DirectComposition]","IDCompositionDevice3 interface","IDCompositionDevice3 interface [DirectComposition]","CreateTurbulenceEffect method","IDCompositionDevice3.CreateTurbulenceEffect","IDCompositionDevice3::CreateTurbulenceEffect","dcomp/IDCompositionDevice3::CreateTurbulenceEffect","directcomp.idcompositiondevice3_createturbulenceeffect"]
old-location: directcomp\idcompositiondevice3_createturbulenceeffect.htm
tech.root: directcomp
ms.assetid: 40BCD422-7545-4CB9-9C8E-2F0D2B4E6C51
ms.date: 12/05/2018
ms.keywords: CreateTurbulenceEffect, CreateTurbulenceEffect method [DirectComposition], CreateTurbulenceEffect method [DirectComposition],IDCompositionDevice3 interface, IDCompositionDevice3 interface [DirectComposition],CreateTurbulenceEffect method, IDCompositionDevice3.CreateTurbulenceEffect, IDCompositionDevice3::CreateTurbulenceEffect, dcomp/IDCompositionDevice3::CreateTurbulenceEffect, directcomp.idcompositiondevice3_createturbulenceeffect
req.header: dcomp.h
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
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDCompositionDevice3::CreateTurbulenceEffect
 - dcomp/IDCompositionDevice3::CreateTurbulenceEffect
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dcomp.dll
api_name:
 - IDCompositionDevice3.CreateTurbulenceEffect
---

# IDCompositionDevice3::CreateTurbulenceEffect


## -description

Creates an instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>.

## -parameters

### -param turbulenceEffect [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>**</b>

Receives the created instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionturbulenceeffect">IDCompositionTurbulenceEffect</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice3">IDCompositionDevice3</a>