---
UID: NN:directmanipulation.IDirectManipulationCompositor
title: IDirectManipulationCompositor (directmanipulation.h)
description: Represents a compositor object that associates manipulated content with a drawing surface, such as canvas (Windows app using JavaScript) or Canvas (Windows Store app using C++, C#, or Visual Basic).
helpviewer_keywords: ["IDirectManipulationCompositor","IDirectManipulationCompositor interface [Direct Manipulation]","IDirectManipulationCompositor interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationcompositor","directmanipulation/IDirectManipulationCompositor"]
old-location: directmanipulation\idirectmanipulationcompositor.htm
tech.root: directmanipulation
ms.assetid: b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1
ms.date: 12/05/2018
ms.keywords: IDirectManipulationCompositor, IDirectManipulationCompositor interface [Direct Manipulation], IDirectManipulationCompositor interface [Direct Manipulation],described, directmanipulation.idirectmanipulationcompositor, directmanipulation/IDirectManipulationCompositor
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
 - IDirectManipulationCompositor
 - directmanipulation/IDirectManipulationCompositor
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
 - IDirectManipulationCompositor
---

# IDirectManipulationCompositor interface


## -description

Represents a compositor object that associates manipulated content with a drawing surface, such as <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element/canvas">canvas</a> (Windows app using JavaScript) or <a href="/previous-versions/windows/silverlight/dotnet-windows-silverlight/ms609101(v=vs.95)
">Canvas</a> (Windows Store app using C++, C#, or Visual Basic).

## -inheritance

The <b>IDirectManipulationCompositor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectManipulationCompositor</b> also has these types of members:

## -remarks

The content of a <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> viewport must be manually updated during an input event for custom implementations of <b>IDirectManipulationCompositor</b>. Call <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationupdatemanager-update">Update</a> to redraw the content within the viewport. 

You specify manual mode on a viewport by calling either of these functions:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportoptions">SetViewportOptions</a>, with <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_viewport_options">DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE</a> specified.</li>
<li>
<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setupdatemode">SetUpdateMode</a>, with <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_input_mode">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> specified.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor2">IDirectManipulationCompositor2</a>
