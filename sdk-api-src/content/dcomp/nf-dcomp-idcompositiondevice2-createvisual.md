---
UID: NF:dcomp.IDCompositionDevice2.CreateVisual
title: IDCompositionDevice2::CreateVisual (dcomp.h)
description: Creates a new visual object.
helpviewer_keywords: ["CreateVisual","CreateVisual method [DirectComposition]","CreateVisual method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","CreateVisual method","IDCompositionDevice2.CreateVisual","IDCompositionDevice2::CreateVisual","dcomp/IDCompositionDevice2::CreateVisual","directcomp.idcompositiondevice2_createvisual"]
old-location: directcomp\idcompositiondevice2_createvisual.htm
tech.root: directcomp
ms.assetid: CCF66B7A-5847-425C-92A4-969C8B915132
ms.date: 12/05/2018
ms.keywords: CreateVisual, CreateVisual method [DirectComposition], CreateVisual method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],CreateVisual method, IDCompositionDevice2.CreateVisual, IDCompositionDevice2::CreateVisual, dcomp/IDCompositionDevice2::CreateVisual, directcomp.idcompositiondevice2_createvisual
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
 - IDCompositionDevice2::CreateVisual
 - dcomp/IDCompositionDevice2::CreateVisual
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
 - IDCompositionDevice2.CreateVisual
---

# IDCompositionDevice2::CreateVisual


## -description

Creates a new visual object.

## -parameters

### -param visual [out]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual2">IDCompositionVisual2</a>**</b>

The new visual object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A new visual object has a static value of zero for the OffsetX and OffsetY properties, and NULL for the Transform, Clip, and Content properties. Initially, the visual  does not cause the contents of a window to change. The visual must be added as a child of another visual, or as the root of a composition target, before it can affect the appearance of a window.

## -see-also

<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiontarget-setroot">IDCompositionTarget::SetRoot</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-addvisual">IDCompositionVisual::AddVisual</a>
