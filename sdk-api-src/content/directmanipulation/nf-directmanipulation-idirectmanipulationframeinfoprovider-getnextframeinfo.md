---
UID: NF:directmanipulation.IDirectManipulationFrameInfoProvider.GetNextFrameInfo
title: IDirectManipulationFrameInfoProvider::GetNextFrameInfo (directmanipulation.h)
description: Retrieves the composition timing information from the compositor.
helpviewer_keywords: ["GetNextFrameInfo","GetNextFrameInfo method [Direct Manipulation]","GetNextFrameInfo method [Direct Manipulation]","IDirectManipulationFrameInfoProvider interface","IDirectManipulationFrameInfoProvider interface [Direct Manipulation]","GetNextFrameInfo method","IDirectManipulationFrameInfoProvider.GetNextFrameInfo","IDirectManipulationFrameInfoProvider::GetNextFrameInfo","directmanipulation.idirectmanipulationframeinfoprovider_getnextframeinfo","directmanipulation/IDirectManipulationFrameInfoProvider::GetNextFrameInfo"]
old-location: directmanipulation\idirectmanipulationframeinfoprovider_getnextframeinfo.htm
tech.root: directmanipulation
ms.assetid: 3f561b81-241f-4f7a-bb5f-a89faf253c98
ms.date: 12/05/2018
ms.keywords: GetNextFrameInfo, GetNextFrameInfo method [Direct Manipulation], GetNextFrameInfo method [Direct Manipulation],IDirectManipulationFrameInfoProvider interface, IDirectManipulationFrameInfoProvider interface [Direct Manipulation],GetNextFrameInfo method, IDirectManipulationFrameInfoProvider.GetNextFrameInfo, IDirectManipulationFrameInfoProvider::GetNextFrameInfo, directmanipulation.idirectmanipulationframeinfoprovider_getnextframeinfo, directmanipulation/IDirectManipulationFrameInfoProvider::GetNextFrameInfo
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
 - IDirectManipulationFrameInfoProvider::GetNextFrameInfo
 - directmanipulation/IDirectManipulationFrameInfoProvider::GetNextFrameInfo
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
 - IDirectManipulationFrameInfoProvider.GetNextFrameInfo
---

# IDirectManipulationFrameInfoProvider::GetNextFrameInfo


## -description

Retrieves the composition timing information from the compositor.

## -parameters

### -param time [out]

The current time, in milliseconds.

### -param processTime [out]

The time, in milliseconds, when the compositor begins constructing the next frame.

### -param compositionTime [out]

The time, in milliseconds, when the compositor finishes composing and drawing the next frame on the screen.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The system implementation of <a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider">IDirectManipulationFrameInfoProvider</a> uses <a href="/windows/desktop/directcomp/directcomposition-portal">DirectComposition</a>. <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-getframestatistics">GetFrameStatistics</a> is used to calculate the parameter values for <b>GetNextFrameInfo</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcompositor">IDirectManipulationCompositor</a>



<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationframeinfoprovider">IDirectManipulationFrameInfoProvider</a>