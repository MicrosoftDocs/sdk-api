---
UID: NF:dcomp.IDCompositionVisual.AddVisual
title: IDCompositionVisual::AddVisual (dcomp.h)
description: Adds a new child visual to the children list of this visual.
helpviewer_keywords: ["AddVisual","AddVisual method [DirectComposition]","AddVisual method [DirectComposition]","IDCompositionVisual interface","IDCompositionVisual interface [DirectComposition]","AddVisual method","IDCompositionVisual.AddVisual","IDCompositionVisual::AddVisual","dcomp/IDCompositionVisual::AddVisual","directcomp.idcompositionvisual_addvisual"]
old-location: directcomp\idcompositionvisual_addvisual.htm
tech.root: directcomp
ms.assetid: e1124df5-7795-49c3-a640-f218cfdd4f1d
ms.date: 12/05/2018
ms.keywords: AddVisual, AddVisual method [DirectComposition], AddVisual method [DirectComposition],IDCompositionVisual interface, IDCompositionVisual interface [DirectComposition],AddVisual method, IDCompositionVisual.AddVisual, IDCompositionVisual::AddVisual, dcomp/IDCompositionVisual::AddVisual, directcomp.idcompositionvisual_addvisual
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
 - IDCompositionVisual::AddVisual
 - dcomp/IDCompositionVisual::AddVisual
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
 - IDCompositionVisual.AddVisual
---

# IDCompositionVisual::AddVisual


## -description

Adds a new child visual to the children list of this visual.

## -parameters

### -param visual [in]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>*</b>

The child visual to add. This parameter must not be NULL.

### -param insertAbove [in]

Type: <b>BOOL</b>

TRUE to place the new child visual in front of the visual specified by the <i>referenceVisual</i> parameter, or FALSE to place it behind <i>referenceVisual</i>.

### -param referenceVisual [in, optional]

Type: <b><a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>*</b>

The existing child visual next to which the new visual should be added.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

Child visuals are arranged in an ordered list. The contents of a child visual are drawn in front of (or above) the contents of its parent visual,  but behind (or below) the contents of its children.

The <i>referenceVisual</i> parameter must be an existing child of the parent visual, or it must be NULL. The <i>insertAbove</i> parameter indicates whether the new child should be rendered immediately above the reference visual in the Z order, or immediately below it.

If the <i>referenceVisual</i> parameter is NULL, the specified visual is rendered above or below all children of the parent visual, depending on the value of the <i>insertAbove</i> parameter. If <i>insertAbove</i> is TRUE, the new child visual is above no sibling, therefore it is rendered  below all of its siblings. Conversely, if <i>insertAbove</i> is FALSE, the visual is below no sibling, therefore it is rendered above all of its siblings.

The visual specified by the <i>visual</i> parameter cannot be either a child of a single other visual, or the root of a visual tree that is associated with a composition target. If <i>visual</i> is already a child of another visual, <b>AddVisual</b> fails. The child visual must be removed from the children list of its previous parent before adding it to the children list of the new parent. If <i>visual</i> is the root of a visual tree, the visual must be dissociated from that visual tree before adding it to the children list of the new parent. To dissociate the visual from a visual tree, call the <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiontarget-setroot">IDCompositionTarget::SetRoot</a> method and specify either a different visual or NULL as the <i>visual</i> parameter.

A child visual need not have been created by the same <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> interface as its parent. When visuals from different devices are combined in the same visual tree,  Microsoft DirectComposition composes the  tree as it normally would, except that changes to a particular visual take effect only when <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-commit">IDCompositionDevice::Commit</a> is called on the device object that created the visual. The ability to combine visuals from different devices  enables multiple threads to create and manipulate a single visual tree while maintaining independent devices that can be used to commit changes asynchronously

This method fails if <i>visual</i> or <i>referenceVisual</i> is an invalid pointer, or if the visual referenced by the <i>referenceVisual</i> parameter is not a child of the parent visual. These  interfaces cannot be custom implementations; only interfaces created by DirectComposition can be used with this method.



#### Examples

For an example, see <a href="/windows/desktop/directcomp/how-to--build-a-visual-tree">How to Build a Simple Visual Tree</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-createvisual">IDCompositionDevice::CreateVisual</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiontarget-setroot">IDCompositionTarget::SetRoot</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-removeallvisuals">IDCompositionVisual::RemoveAllVisuals</a>



<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositionvisual-removevisual">IDCompositionVisual::RemoveVisual</a>