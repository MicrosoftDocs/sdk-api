---
UID: NF:directmanipulation.IDirectManipulationPrimaryContent.SetVerticalAlignment
title: IDirectManipulationPrimaryContent::SetVerticalAlignment (directmanipulation.h)
description: Specifies the vertical alignment of the primary content in the viewport.
helpviewer_keywords: ["IDirectManipulationPrimaryContent interface [Direct Manipulation]","SetVerticalAlignment method","IDirectManipulationPrimaryContent.SetVerticalAlignment","IDirectManipulationPrimaryContent::SetVerticalAlignment","SetVerticalAlignment","SetVerticalAlignment method [Direct Manipulation]","SetVerticalAlignment method [Direct Manipulation]","IDirectManipulationPrimaryContent interface","directmanipulation.idirectmanipulationprimarycontent_setverticalalignment","directmanipulation/IDirectManipulationPrimaryContent::SetVerticalAlignment"]
old-location: directmanipulation\idirectmanipulationprimarycontent_setverticalalignment.htm
tech.root: directmanipulation
ms.assetid: 111f0358-0955-4ebb-b273-c17d3fb84d75
ms.date: 12/05/2018
ms.keywords: IDirectManipulationPrimaryContent interface [Direct Manipulation],SetVerticalAlignment method, IDirectManipulationPrimaryContent.SetVerticalAlignment, IDirectManipulationPrimaryContent::SetVerticalAlignment, SetVerticalAlignment, SetVerticalAlignment method [Direct Manipulation], SetVerticalAlignment method [Direct Manipulation],IDirectManipulationPrimaryContent interface, directmanipulation.idirectmanipulationprimarycontent_setverticalalignment, directmanipulation/IDirectManipulationPrimaryContent::SetVerticalAlignment
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
 - IDirectManipulationPrimaryContent::SetVerticalAlignment
 - directmanipulation/IDirectManipulationPrimaryContent::SetVerticalAlignment
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
 - IDirectManipulationPrimaryContent.SetVerticalAlignment
---

# IDirectManipulationPrimaryContent::SetVerticalAlignment


## -description

Specifies the vertical alignment of the primary content in the viewport.

## -parameters

### -param alignment [in]

One or more values from <a href="/previous-versions/windows/desktop/api/directmanipulation/ne-directmanipulation-directmanipulation_verticalalignment">DIRECTMANIPULATION_VERTICALALIGNMENT</a>.

<div class="alert"><b>Note</b>  You cannot combine <b>DIRECTMANIPULATION_VERTICALALIGNMENT_TOP</b>, <b>DIRECTMANIPULATION_VERTICALALIGNMENT_CENTER</b>, or <b>DIRECTMANIPULATION_VERTICALALIGNMENT_BOTTOM</b>. <b>DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER</b> can be combined with any option but cannot be configured by itself.</div>
<div> </div>

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you have activated a configuration consisting only of zoom or zoom inertia, specify <b>DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER</b> to respect the zoom center point.


#### Examples

The following example shows how to use this method.


```
HRESULT hr = pContent->SetVerticalAlignment(
    DIRECTMANIPULATION_VERTICALALIGNMENT_CENTER| DIRECTMANIPULATION_VERTICALALIGNMENT_UNLOCKCENTER);
```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>