---
UID: NF:directmanipulation.IDirectManipulationCompositor2.AddContentWithCrossProcessChaining
title: IDirectManipulationCompositor2::AddContentWithCrossProcessChaining (directmanipulation.h)
description: Associates content (owned by the component host) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals.
helpviewer_keywords: ["AddContentWithCrossProcessChaining","AddContentWithCrossProcessChaining method [Direct Manipulation]","AddContentWithCrossProcessChaining method [Direct Manipulation]","IDirectManipulationCompositor2 interface","IDirectManipulationCompositor2 interface [Direct Manipulation]","AddContentWithCrossProcessChaining method","IDirectManipulationCompositor2.AddContentWithCrossProcessChaining","IDirectManipulationCompositor2::AddContentWithCrossProcessChaining","directmanipulation.idirectmanipulationcompositor2_addcontentwithcrossprocesschaining","directmanipulation/IDirectManipulationCompositor2::AddContentWithCrossProcessChaining"]
old-location: directmanipulation\idirectmanipulationcompositor2_addcontentwithcrossprocesschaining.htm
tech.root: directmanipulation
ms.assetid: dd6052df-30b5-4872-89a7-b98126fcd44d
ms.date: 12/05/2018
ms.keywords: AddContentWithCrossProcessChaining, AddContentWithCrossProcessChaining method [Direct Manipulation], AddContentWithCrossProcessChaining method [Direct Manipulation],IDirectManipulationCompositor2 interface, IDirectManipulationCompositor2 interface [Direct Manipulation],AddContentWithCrossProcessChaining method, IDirectManipulationCompositor2.AddContentWithCrossProcessChaining, IDirectManipulationCompositor2::AddContentWithCrossProcessChaining, directmanipulation.idirectmanipulationcompositor2_addcontentwithcrossprocesschaining, directmanipulation/IDirectManipulationCompositor2::AddContentWithCrossProcessChaining
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Directmanipulation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectManipulationCompositor2::AddContentWithCrossProcessChaining
 - directmanipulation/IDirectManipulationCompositor2::AddContentWithCrossProcessChaining
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - directmanipulation.h
api_name:
 - IDirectManipulationCompositor2.AddContentWithCrossProcessChaining
---

# IDirectManipulationCompositor2::AddContentWithCrossProcessChaining


## -description

Associates content (owned by the component host) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals. Represents a compositor object that associates manipulated content with drawing surfaces across multiple processes.

## -parameters

### -param content [in]

The content to add to the composition tree.

<i>content</i> is placed  between <i>parentVisual</i> and <i>childVisual</i> in the composition tree. 

Only primary content, created at the same time as the viewport, is valid.

### -param device [in]

The device used to compose the content. 

<div class="alert"><b>Note</b>  <i>device</i> is created by the application.</div>
<div> </div>

### -param parentVisual [in]

The parent visuals in the composition tree of the content being added.

<i>parentVisual</i> must also be a parent of <i>childVisual</i> in the composition tree.

### -param childVisual [in]

The child visuals in the composition tree of the content being added.

<i>parentVisual</i> must also be a parent of <i>childVisual</i> in the composition tree.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method inserts a small visual tree (owned by the <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> device) between the <i>parentVisual</i> and the <i>childVisual</i>. Transforms can then be applied to the inserted content.  


All content, regardless of type, must be added to the compositor. 

If the application uses a system-provided <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>:

<ul>
<li><i>device</i> must be an  <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> object, and parent and child visuals must be <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a> objects.</li>
<li><i>device</i>, <i>parentVisual</i>, and <i>childVisual</i> cannot be NULL. </li>
<li><i>device</i>, <i>parentVisual</i>, and <i>childVisual</i> objects are created and owned by the application.
</li>
<li>When content is added to the composition tree using this method, the new composition visuals are inserted between <i>parentVisual</i> and <i>childVisual</i>. The new visuals should not be destroyed until they are disassociated from the compositor with <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcompositor-removecontent">RemoveContent</a>.</li>
</ul>
If the application uses a custom implementation of <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>:

<ul>
<li><i>device</i>, <i>parentVisual</i>, and <i>childVisual</i> must be a valid type for the compositor. They do not have to be <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a> or <a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositionvisual">IDCompositionVisual</a> objects.</li>
<li><i>device</i>, <i>parentVisual</i>, and <i>childVisual</i> can be NULL, depending on the compositor. </li>
</ul>
The cross-process pointer events (<a href="/previous-versions/windows/desktop/inputmsg/wm-pointerroutedaway">WM_POINTERROUTEDAWAY</a>, <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerroutedreleased">WM_POINTERROUTEDRELEASED</a>, and <a href="/previous-versions/windows/desktop/inputmsg/wm-pointerroutedto">WM_POINTERROUTEDTO</a>) should be handled appropriately.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor2">IDirectManipulationCompositor2</a>



<a href="/previous-versions/windows/desktop/inputmsg/wm-pointerroutedaway">WM_POINTERROUTEDAWAY</a>



<a href="/previous-versions/windows/desktop/inputmsg/wm-pointerroutedreleased">WM_POINTERROUTEDRELEASED</a>



<a href="/previous-versions/windows/desktop/inputmsg/wm-pointerroutedto">WM_POINTERROUTEDTO</a>