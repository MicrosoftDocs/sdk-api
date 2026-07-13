---
UID: NF:dcomp.IDCompositionDevice2.CreateAnimation
title: IDCompositionDevice2::CreateAnimation (dcomp.h)
description: Creates an animation object that is used to animate one or more scalar properties of one or more Microsoft DirectComposition objects. (IDCompositionDevice2.CreateAnimation)
helpviewer_keywords: ["CreateAnimation","CreateAnimation method [DirectComposition]","CreateAnimation method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateAnimation method","IDCompositionDevice2.CreateAnimation","IDCompositionDevice2::CreateAnimation","dcomp/IDCompositionDevice2::CreateAnimation","directcomp.idcompositiondevice2_createanimation"]
old-location: directcomp\idcompositiondevice2_createanimation.htm
tech.root: directcomp
ms.assetid: 6F15F6CD-E2EE-42E5-AF46-01A9A28F4896
ms.date: 12/05/2018
ms.keywords: CreateAnimation, CreateAnimation method [DirectComposition], CreateAnimation method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateAnimation method, IDCompositionDevice2.CreateAnimation, IDCompositionDevice2::CreateAnimation, dcomp/IDCompositionDevice2::CreateAnimation, directcomp.idcompositiondevice2_createanimation
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
 - IDCompositionDevice2::CreateAnimation
 - dcomp/IDCompositionDevice2::CreateAnimation
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
 - IDCompositionDevice2.CreateAnimation
---

# IDCompositionDevice2::CreateAnimation


## -description

Creates an animation object that is used to animate one or more scalar properties of one or more Microsoft DirectComposition objects.

## -parameters

### -param animation [out]

Type: <b><a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a>**</b>

The new animation object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A number of DirectComposition object properties can have an animation object as the value of the property. When a property has an animation object as its value, DirectComposition redraws the visual at the refresh rate to reflect the changing value of the property that is being animated.

A newly created animation object does not have any animation segments associated with it. An application must use the methods of the <a href="/windows/desktop/api/dcompanimation/nn-dcompanimation-idcompositionanimation">IDCompositionAnimation</a> interface to build an animation function before setting the animation object as the property of another DirectComposition object.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>
