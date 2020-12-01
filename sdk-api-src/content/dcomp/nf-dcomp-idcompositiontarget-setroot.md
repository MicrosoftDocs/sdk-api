---
UID: NF:dcomp.IDCompositionTarget.SetRoot
title: IDCompositionTarget::SetRoot (dcomp.h)
description: Sets a visual object as the new root object of a visual tree.
helpviewer_keywords: ["IDCompositionTarget interface [DirectComposition]","SetRoot method","IDCompositionTarget.SetRoot","IDCompositionTarget::SetRoot","SetRoot","SetRoot method [DirectComposition]","SetRoot method [DirectComposition]","IDCompositionTarget interface","dcomp/IDCompositionTarget::SetRoot","directcomp.idcompositiontarget_setroot"]
old-location: directcomp\idcompositiontarget_setroot.htm
tech.root: directcomp
ms.assetid: febbef70-fc21-4295-93c5-2f9f52434aae
ms.date: 12/05/2018
ms.keywords: IDCompositionTarget interface [DirectComposition],SetRoot method, IDCompositionTarget.SetRoot, IDCompositionTarget::SetRoot, SetRoot, SetRoot method [DirectComposition], SetRoot method [DirectComposition],IDCompositionTarget interface, dcomp/IDCompositionTarget::SetRoot, directcomp.idcompositiontarget_setroot
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IDCompositionTarget::SetRoot
 - dcomp/IDCompositionTarget::SetRoot
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
 - IDCompositionTarget.SetRoot
---

# IDCompositionTarget::SetRoot


## -description

Sets a visual object as the new root object of a visual tree.

## -parameters

### -param visual [in, optional]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>*</b>

The visual object that is the new root of this visual tree. This parameter can be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

A visual can be either the root of a single visual tree, or a child of another visual, but it cannot be both at the same time. This method fails if the <i>visual</i> parameter is already the root of another visual tree, or is a child of another visual.

If <i>visual</i> is NULL, the visual tree is empty. If there was a previous non-NULL root visual, that visual becomes available for use as the root of another visual tree, or as a child of another visual.


#### Examples

For an example, see <a href="/windows/desktop/directcomp/how-to--build-a-visual-tree">How to Build a Simple Visual Tree</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createvisual">IDCompositionDevice::CreateVisual</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiontarget">IDCompositionTarget</a>