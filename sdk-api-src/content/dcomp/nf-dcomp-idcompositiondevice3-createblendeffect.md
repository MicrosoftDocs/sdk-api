---
UID: NF:dcomp.IDCompositionDevice3.CreateBlendEffect
title: IDCompositionDevice3::CreateBlendEffect (dcomp.h)
description: Creates an instance of IDCompositionBlendEffect.
helpviewer_keywords: ["CreateBlendEffect","CreateBlendEffect method [DirectComposition]","CreateBlendEffect method [DirectComposition]","IDCompositionDevice3 interface","IDCompositionDevice3 interface [DirectComposition]","CreateBlendEffect method","IDCompositionDevice3.CreateBlendEffect","IDCompositionDevice3::CreateBlendEffect","dcomp/IDCompositionDevice3::CreateBlendEffect","directcomp.idcompositiondevice3_createblendeffect"]
old-location: directcomp\idcompositiondevice3_createblendeffect.htm
tech.root: directcomp
ms.assetid: 20E05261-E5B6-4F48-B595-F2AD8B96AB2E
ms.date: 12/05/2018
ms.keywords: CreateBlendEffect, CreateBlendEffect method [DirectComposition], CreateBlendEffect method [DirectComposition],IDCompositionDevice3 interface, IDCompositionDevice3 interface [DirectComposition],CreateBlendEffect method, IDCompositionDevice3.CreateBlendEffect, IDCompositionDevice3::CreateBlendEffect, dcomp/IDCompositionDevice3::CreateBlendEffect, directcomp.idcompositiondevice3_createblendeffect
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
 - IDCompositionDevice3::CreateBlendEffect
 - dcomp/IDCompositionDevice3::CreateBlendEffect
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
 - IDCompositionDevice3.CreateBlendEffect
---

# IDCompositionDevice3::CreateBlendEffect


## -description

Creates an instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionblendeffect">IDCompositionBlendEffect</a>.

## -parameters

### -param blendEffect [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionblendeffect">IDCompositionBlendEffect</a>**</b>

Receives the created instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionblendeffect">IDCompositionBlendEffect</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice3">IDCompositionDevice3</a>