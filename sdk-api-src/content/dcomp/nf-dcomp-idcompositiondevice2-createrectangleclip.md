---
UID: NF:dcomp.IDCompositionDevice2.CreateRectangleClip
title: IDCompositionDevice2::CreateRectangleClip (dcomp.h)
description: Creates a clip object that can be used to restrict the rendering of a visual subtree to a rectangular area. (IDCompositionDevice2.CreateRectangleClip)
helpviewer_keywords: ["CreateRectangleClip","CreateRectangleClip method [DirectComposition]","CreateRectangleClip method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateRectangleClip method","IDCompositionDevice2.CreateRectangleClip","IDCompositionDevice2::CreateRectangleClip","dcomp/IDCompositionDevice2::CreateRectangleClip","directcomp.idcompositiondevice2_createrectangleclip"]
old-location: directcomp\idcompositiondevice2_createrectangleclip.htm
tech.root: directcomp
ms.assetid: 5CD7BC88-EF6F-4FEE-940B-710CB56D8E78
ms.date: 12/05/2018
ms.keywords: CreateRectangleClip, CreateRectangleClip method [DirectComposition], CreateRectangleClip method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateRectangleClip method, IDCompositionDevice2.CreateRectangleClip, IDCompositionDevice2::CreateRectangleClip, dcomp/IDCompositionDevice2::CreateRectangleClip, directcomp.idcompositiondevice2_createrectangleclip
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
 - IDCompositionDevice2::CreateRectangleClip
 - dcomp/IDCompositionDevice2::CreateRectangleClip
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
 - IDCompositionDevice2.CreateRectangleClip
---

# IDCompositionDevice2::CreateRectangleClip


## -description

Creates a clip object that can be used to restrict the rendering of  a visual subtree to a rectangular area.

## -parameters

### -param clip [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionrectangleclip">IDCompositionRectangleClip</a>**</b>

The new clip object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A newly created clip object has a value of -2^21 for the left and top properties, and a value of 2^21 for the right and bottom properties, effectively making it a no-op clip object.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>

<a href="/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)">IDCompositionVisual::SetClip</a>
