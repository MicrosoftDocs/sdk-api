---
UID: NF:directmanipulation.IDirectManipulationCompositor.AddContent
title: IDirectManipulationCompositor::AddContent (directmanipulation.h)
description: Associates content (owned by the caller) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals.
helpviewer_keywords: ["AddContent","AddContent method [Direct Manipulation]","AddContent method [Direct Manipulation]","IDirectManipulationCompositor interface","IDirectManipulationCompositor interface [Direct Manipulation]","AddContent method","IDirectManipulationCompositor.AddContent","IDirectManipulationCompositor::AddContent","directmanipulation.idirectmanipulationcompositor_addcontent","directmanipulation/IDirectManipulationCompositor::AddContent"]
old-location: directmanipulation\idirectmanipulationcompositor_addcontent.htm
tech.root: directmanipulation
ms.assetid: 16c1a911-43cb-4c18-9e29-12a69b715e6a
ms.date: 12/05/2018
ms.keywords: AddContent, AddContent method [Direct Manipulation], AddContent method [Direct Manipulation],IDirectManipulationCompositor interface, IDirectManipulationCompositor interface [Direct Manipulation],AddContent method, IDirectManipulationCompositor.AddContent, IDirectManipulationCompositor::AddContent, directmanipulation.idirectmanipulationcompositor_addcontent, directmanipulation/IDirectManipulationCompositor::AddContent
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - IDirectManipulationCompositor::AddContent
 - directmanipulation/IDirectManipulationCompositor::AddContent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationCompositor.AddContent
---

# IDirectManipulationCompositor::AddContent


## -description

Associates content (owned by the caller) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals.

## -parameters

### -param content [in]

The content to add to the composition tree.

<i>content</i> is placed  between <i>parentVisual</i> and <i>childVisual</i> in the composition tree.

### -param device [in, optional]

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


All content, regardless of type, must be added to the compositor. This can be primary content, obtained from the viewport by calling <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-getprimarycontent">GetPrimaryContent</a>, or secondary content, such as a panning indicator, created by calling <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationmanager-createcontent">CreateContent</a>.


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

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>