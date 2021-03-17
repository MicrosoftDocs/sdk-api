---
UID: NF:directmanipulation.IDirectManipulationViewport.GetTag
title: IDirectManipulationViewport::GetTag (directmanipulation.h)
description: Gets the tag value of a viewport.
helpviewer_keywords: ["GetTag","GetTag method [Direct Manipulation]","GetTag method [Direct Manipulation]","IDirectManipulationViewport interface","IDirectManipulationViewport interface [Direct Manipulation]","GetTag method","IDirectManipulationViewport.GetTag","IDirectManipulationViewport::GetTag","directmanipulation.idirectmanipulationviewport_gettag","directmanipulation/IDirectManipulationViewport::GetTag"]
old-location: directmanipulation\idirectmanipulationviewport_gettag.htm
tech.root: directmanipulation
ms.assetid: 7523a99b-de43-4efe-ae22-6632167c039a
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Direct Manipulation], GetTag method [Direct Manipulation],IDirectManipulationViewport interface, IDirectManipulationViewport interface [Direct Manipulation],GetTag method, IDirectManipulationViewport.GetTag, IDirectManipulationViewport::GetTag, directmanipulation.idirectmanipulationviewport_gettag, directmanipulation/IDirectManipulationViewport::GetTag
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
 - IDirectManipulationViewport::GetTag
 - directmanipulation/IDirectManipulationViewport::GetTag
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
 - IDirectManipulationViewport.GetTag
---

# IDirectManipulationViewport::GetTag


## -description

Gets the tag value of a viewport.

## -parameters

### -param riid [in]

IID to the interface.

### -param object [out, optional]

The object portion of the tag.

### -param id [out, optional]

The identifier portion of the tag.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A tag is a pairing of an integer ID with a Component Object Model (COM) object. It can be used by an app to identify the viewport.

The out parameters are optional, so the method can return an ID, the viewport object, or both.



#### Examples

The following example show how to use this method.


```
IUnknown* pUnk;
UINT32 id;

HRESULT hr = pRegion->GetTag(IID_PPV_ARGS(&pUnk), &id); 


```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationviewport">IDirectManipulationViewport</a>