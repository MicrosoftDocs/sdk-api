---
UID: NN:directmanipulation.IDirectManipulationCompositor2
title: IDirectManipulationCompositor2 (directmanipulation.h)
description: Represents a compositor object that associates manipulated content with drawing surfaces across multiple processes.
helpviewer_keywords: ["IDirectManipulationCompositor2","IDirectManipulationCompositor2 interface [Direct Manipulation]","IDirectManipulationCompositor2 interface [Direct Manipulation]","described","directmanipulation.idirectmanipulationcompositor2","directmanipulation/IDirectManipulationCompositor2"]
old-location: directmanipulation\idirectmanipulationcompositor2.htm
tech.root: directmanipulation
ms.assetid: e428ddaa-3913-498a-a3fd-bed10289cd8d
ms.date: 12/05/2018
ms.keywords: IDirectManipulationCompositor2, IDirectManipulationCompositor2 interface [Direct Manipulation], IDirectManipulationCompositor2 interface [Direct Manipulation],described, directmanipulation.idirectmanipulationcompositor2, directmanipulation/IDirectManipulationCompositor2
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - IDirectManipulationCompositor2
 - directmanipulation/IDirectManipulationCompositor2
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
 - IDirectManipulationCompositor2
---

# IDirectManipulationCompositor2 interface


## -description

Represents a compositor object that associates manipulated content with drawing surfaces across multiple processes.

## -inheritance

The <b>IDirectManipulationCompositor2</b> interface inherits from <b>IDirectManipulationCompositor</b>. <b>IDirectManipulationCompositor2</b> also has these types of members:

## -remarks

The content of a <a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-portal">Direct Manipulation</a> viewport must be manually updated during an input event for custom implementations of <b>IDirectManipulationCompositor2</b>. Call <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationupdatemanager-update">Update</a> to redraw the content within the viewport. 

You specify manual mode on a viewport by calling either of these functions:

<ul>
<li>
<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setviewportoptions">SetViewportOptions</a>, with <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_viewport_options">DIRECTMANIPULATION_VIEWPORT_OPTIONS_MANUALUPDATE</a> specified.</li>
<li>
<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationviewport-setupdatemode">SetUpdateMode</a>, with <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_input_mode">DIRECTMANIPULATION_INPUT_MODE_MANUAL</a> specified.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/directmanipulation/direct-manipulation-interfaces">Direct Manipulation Interfaces</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>
