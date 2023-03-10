---
UID: NF:directmanipulation.IDirectManipulationViewport.GetPrimaryContent
title: IDirectManipulationViewport::GetPrimaryContent (directmanipulation.h)
description: Gets the primary content of a viewport that implements IDirectManipulationContent and IDirectManipulationPrimaryContent.
helpviewer_keywords: ["GetPrimaryContent","GetPrimaryContent method [Direct Manipulation]","GetPrimaryContent method [Direct Manipulation]","IDirectManipulationViewport interface","IDirectManipulationViewport interface [Direct Manipulation]","GetPrimaryContent method","IDirectManipulationViewport.GetPrimaryContent","IDirectManipulationViewport::GetPrimaryContent","directmanipulation.idirectmanipulationviewport_getprimarycontent","directmanipulation/IDirectManipulationViewport::GetPrimaryContent"]
old-location: directmanipulation\idirectmanipulationviewport_getprimarycontent.htm
tech.root: directmanipulation
ms.assetid: 1aa70be3-9e95-4c35-8cca-45c1b238961e
ms.date: 12/05/2018
ms.keywords: GetPrimaryContent, GetPrimaryContent method [Direct Manipulation], GetPrimaryContent method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],GetPrimaryContent method, IDirectManipulationViewport.GetPrimaryContent, IDirectManipulationViewport::GetPrimaryContent, directmanipulation.idirectmanipulationviewport_getprimarycontent, directmanipulation/IDirectManipulationViewport::GetPrimaryContent
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
 - IDirectManipulationViewport::GetPrimaryContent
 - directmanipulation/IDirectManipulationViewport::GetPrimaryContent
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
 - IDirectManipulationViewport.GetPrimaryContent
---

# IDirectManipulationViewport::GetPrimaryContent


## -description

Gets the primary content of a viewport that implements <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a> and <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>. 

Primary content is an element that gets transformed (e.g. moved, scaled, rotated) in response to a user interaction. Primary content is created at the same time as the viewport and cannot be added or removed.

## -parameters

### -param riid [in]

IID to the interface.

### -param object [out, retval]

The primary content object.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

    This method gets the content of the viewport that implements <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a> and <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationprimarycontent">IDirectManipulationPrimaryContent</a>.



#### Examples

The following example shows how to use this method.


```
IDirectManipulationPrimaryContent *pContent;

HRESULT hr = pRegion->GetPrimaryContent(IID_PPV_ARGS(&pContent));

```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>