---
UID: NF:dcomp.IDCompositionDevice3.CreateSaturationEffect
title: IDCompositionDevice3::CreateSaturationEffect (dcomp.h)
description: Creates an instance of IDCompositionSaturationEffect.
helpviewer_keywords: ["CreateSaturationEffect","CreateSaturationEffect method [DirectComposition]","CreateSaturationEffect method [DirectComposition]","IDCompositionDevice3 interface","IDCompositionDevice3 interface [DirectComposition]","CreateSaturationEffect method","IDCompositionDevice3.CreateSaturationEffect","IDCompositionDevice3::CreateSaturationEffect","dcomp/IDCompositionDevice3::CreateSaturationEffect","directcomp.idcompositiondevice3_createsaturationeffect"]
old-location: directcomp\idcompositiondevice3_createsaturationeffect.htm
tech.root: directcomp
ms.assetid: 19613AF4-6EC0-4918-9FC1-147A04D321CA
ms.date: 12/05/2018
ms.keywords: CreateSaturationEffect, CreateSaturationEffect method [DirectComposition], CreateSaturationEffect method [DirectComposition],IDCompositionDevice3 interface, IDCompositionDevice3 interface [DirectComposition],CreateSaturationEffect method, IDCompositionDevice3.CreateSaturationEffect, IDCompositionDevice3::CreateSaturationEffect, dcomp/IDCompositionDevice3::CreateSaturationEffect, directcomp.idcompositiondevice3_createsaturationeffect
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
 - IDCompositionDevice3::CreateSaturationEffect
 - dcomp/IDCompositionDevice3::CreateSaturationEffect
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
 - IDCompositionDevice3.CreateSaturationEffect
---

# IDCompositionDevice3::CreateSaturationEffect


## -description

Creates an instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsaturationeffect">IDCompositionSaturationEffect</a>.

## -parameters

### -param saturationEffect [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsaturationeffect">IDCompositionSaturationEffect</a>**</b>

Receives the created instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionsaturationeffect">IDCompositionSaturationEffect</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice3">IDCompositionDevice3</a>