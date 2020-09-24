---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetHorizontalAlignment
title: IDirectManipulationPrimaryContent::SetHorizontalAlignment (directmanipulation.h)
description: Sets the horizontal alignment of the primary content relative to the viewport.
helpviewer_keywords: ["IDirectManipulationPrimaryContent interface [Direct Manipulation]","SetHorizontalAlignment method","IDirectManipulationPrimaryContent.SetHorizontalAlignment","IDirectManipulationPrimaryContent::SetHorizontalAlignment","SetHorizontalAlignment","SetHorizontalAlignment method [Direct Manipulation]","SetHorizontalAlignment method [Direct Manipulation]","IDirectManipulationPrimaryContent interface","directmanipulation.idirectmanipulationprimarycontent_sethorizontalalignment","directmanipulation/IDirectManipulationPrimaryContent::SetHorizontalAlignment"]
old-location: directmanipulation\idirectmanipulationprimarycontent_sethorizontalalignment.htm
tech.root: directmanipulation
ms.assetid: 94716ec8-325e-4e9e-9a30-1d9999bdb9c3
ms.date: 12/05/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetHorizontalAlignment method, IDirectManipulationPrimaryContent.SetHorizontalAlignment, IDirectManipulationPrimaryContent::SetHorizontalAlignment, SetHorizontalAlignment, SetHorizontalAlignment method [Direct Manipulation], SetHorizontalAlignment method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_sethorizontalalignment, directmanipulation/IDirectManipulationPrimaryContent::SetHorizontalAlignment
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
 - IDirectManipulationPrimaryContent::SetHorizontalAlignment
 - directmanipulation/IDirectManipulationPrimaryContent::SetHorizontalAlignment
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
 - IDirectManipulationPrimaryContent.SetHorizontalAlignment
---

# IDirectManipulationPrimaryContent::SetHorizontalAlignment


## -description

Sets the horizontal alignment of the primary content relative to the viewport.

## -parameters

### -param alignment [in]

One or more values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_horizontalalignment">DIRECTMANIPULATION_HORIZONTALALIGNMENT</a>. The default is <b>DIRECTMANIPULATION_HORIZONTALALIGNMENT_NONE</b>.

<div class="alert"><b>Note</b>  You cannot combine the following options: DIRECTMANIPULATION_HORIZONTALALIGNMENT_LEFT, DIRECTMANIPULATION-HORIZONTALALIGNMENT_CENTER, DIRECTMANIPULATION_HORIZONTALALIGNMENT_RIGHT. DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER can be combined with any option but cannot be configured by itself.</div>
<div> </div>

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you have activated a configuration consisting only of zoom or zoom inertia, specify DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER to respect the zoom center point.


#### Examples

The following example shows one way to  this method.


```
HRESULT hr = pViewport->SetHorizontalAlignment(
    DIRECTMANIPULATION_HORIZONTALALIGNMENT_CENTER | DIRECTMANIPULATION_HORIZONTALALIGNMENT_UNLOCKCENTER);
```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>