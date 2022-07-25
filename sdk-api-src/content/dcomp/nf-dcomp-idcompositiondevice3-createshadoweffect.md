---
UID: NF:dcomp.IDCompositionDevice3.CreateShadowEffect
title: IDCompositionDevice3::CreateShadowEffect (dcomp.h)
description: Creates an instance of IDCompositionShadowEffect.
helpviewer_keywords: ["CreateShadowEffect","CreateShadowEffect method [DirectComposition]","CreateShadowEffect method [DirectComposition]","IDCompositionDevice3 interface","IDCompositionDevice3 interface [DirectComposition]","CreateShadowEffect method","IDCompositionDevice3.CreateShadowEffect","IDCompositionDevice3::CreateShadowEffect","dcomp/IDCompositionDevice3::CreateShadowEffect","directcomp.idcompositiondevice3_createshadoweffect"]
old-location: directcomp\idcompositiondevice3_createshadoweffect.htm
tech.root: directcomp
ms.assetid: C0A2B599-F061-4312-BDBC-96DF724F02D8
ms.date: 12/05/2018
ms.keywords: CreateShadowEffect, CreateShadowEffect method [DirectComposition], CreateShadowEffect method [DirectComposition],IDCompositionDevice3 interface, IDCompositionDevice3 interface [DirectComposition],CreateShadowEffect method, IDCompositionDevice3.CreateShadowEffect, IDCompositionDevice3::CreateShadowEffect, dcomp/IDCompositionDevice3::CreateShadowEffect, directcomp.idcompositiondevice3_createshadoweffect
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
 - IDCompositionDevice3::CreateShadowEffect
 - dcomp/IDCompositionDevice3::CreateShadowEffect
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
 - IDCompositionDevice3.CreateShadowEffect
---

# IDCompositionDevice3::CreateShadowEffect


## -description

Creates an instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>.

## -parameters

### -param shadowEffect [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>**</b>

Receives the created instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionshadoweffect">IDCompositionShadowEffect</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice3">IDCompositionDevice3</a>