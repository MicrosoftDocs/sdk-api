---
UID: NF:dcomp.IDCompositionDevice2.CreateEffectGroup
title: IDCompositionDevice2::CreateEffectGroup (dcomp.h)
description: Creates an object that represents multiple effects to be applied to a visual subtree. (IDCompositionDevice2.CreateEffectGroup)
helpviewer_keywords: ["CreateEffectGroup","CreateEffectGroup method [DirectComposition]","CreateEffectGroup method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateEffectGroup method","IDCompositionDevice2.CreateEffectGroup","IDCompositionDevice2::CreateEffectGroup","dcomp/IDCompositionDevice2::CreateEffectGroup","directcomp.idcompositiondevice2_createeffectgroup"]
old-location: directcomp\idcompositiondevice2_createeffectgroup.htm
tech.root: directcomp
ms.assetid: 07AF43F9-1050-48C5-B37B-787B5CC60E9D
ms.date: 12/05/2018
ms.keywords: CreateEffectGroup, CreateEffectGroup method [DirectComposition], CreateEffectGroup method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateEffectGroup method, IDCompositionDevice2.CreateEffectGroup, IDCompositionDevice2::CreateEffectGroup, dcomp/IDCompositionDevice2::CreateEffectGroup, directcomp.idcompositiondevice2_createeffectgroup
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDCompositionDevice2::CreateEffectGroup
 - dcomp/IDCompositionDevice2::CreateEffectGroup
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dcomp.dll
api_name:
 - IDCompositionDevice2.CreateEffectGroup
---

# IDCompositionDevice2::CreateEffectGroup


## -description

Creates an object that represents multiple effects to be applied to a visual subtree.

## -parameters

### -param effectGroup [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffectgroup">IDCompositionEffectGroup</a>**</b>

The new effect group object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

An effect group enables an application to apply multiple effects to a single visual subtree. 

A new effect group has a default opacity value of 1.0 and no 3D transformations.

To set the opacity and transform values, use the corresponding methods on the <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositioneffectgroup">IDCompositionEffectGroup</a> that was created.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-seteffect">IDCompositionVisual::SetEffect</a>
