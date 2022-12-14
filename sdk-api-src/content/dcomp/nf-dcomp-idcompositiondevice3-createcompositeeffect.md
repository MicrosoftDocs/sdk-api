---
UID: NF:dcomp.IDCompositionDevice3.CreateCompositeEffect
title: IDCompositionDevice3::CreateCompositeEffect (dcomp.h)
description: Creates an instance of IDCompositionCompositeEffect.
helpviewer_keywords: ["CreateCompositeEffect","CreateCompositeEffect method [DirectComposition]","CreateCompositeEffect method [DirectComposition]","IDCompositionDevice3 interface","IDCompositionDevice3 interface [DirectComposition]","CreateCompositeEffect method","IDCompositionDevice3.CreateCompositeEffect","IDCompositionDevice3::CreateCompositeEffect","dcomp/IDCompositionDevice3::CreateCompositeEffect","directcomp.idcompositiondevice3_createcompositeeffect"]
old-location: directcomp\idcompositiondevice3_createcompositeeffect.htm
tech.root: directcomp
ms.assetid: 9DA1541E-0792-482E-81AF-A6C91665D9D8
ms.date: 12/05/2018
ms.keywords: CreateCompositeEffect, CreateCompositeEffect method [DirectComposition], CreateCompositeEffect method [DirectComposition],IDCompositionDevice3 interface, IDCompositionDevice3 interface [DirectComposition],CreateCompositeEffect method, IDCompositionDevice3.CreateCompositeEffect, IDCompositionDevice3::CreateCompositeEffect, dcomp/IDCompositionDevice3::CreateCompositeEffect, directcomp.idcompositiondevice3_createcompositeeffect
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
 - IDCompositionDevice3::CreateCompositeEffect
 - dcomp/IDCompositionDevice3::CreateCompositeEffect
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
 - IDCompositionDevice3.CreateCompositeEffect
---

# IDCompositionDevice3::CreateCompositeEffect


## -description

Creates an instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncompositeeffect">IDCompositionCompositeEffect</a>.

## -parameters

### -param compositeEffect [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncompositeeffect">IDCompositionCompositeEffect</a>**</b>

Receives the created instance of <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioncompositeeffect">IDCompositionCompositeEffect</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice3">IDCompositionDevice3</a>