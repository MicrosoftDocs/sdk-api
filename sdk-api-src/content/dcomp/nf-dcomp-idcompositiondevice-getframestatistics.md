---
UID: NF:dcomp.IDCompositionDevice.GetFrameStatistics
title: IDCompositionDevice::GetFrameStatistics (dcomp.h)
description: The IDCompositionDevice::GetFrameStatistics method retrieves information from the composition engine about composition times and the frame rate.
helpviewer_keywords: ["GetFrameStatistics","GetFrameStatistics method [DirectComposition]","GetFrameStatistics method [DirectComposition]","IDCompositionDevice interface","IDCompositionDevice interface [DirectComposition]","GetFrameStatistics method","IDCompositionDevice.GetFrameStatistics","IDCompositionDevice::GetFrameStatistics","dcomp/IDCompositionDevice::GetFrameStatistics","directcomp.idcompositiondevice_getframestatistics"]
old-location: directcomp\idcompositiondevice_getframestatistics.htm
tech.root: directcomp
ms.assetid: C4DB7A16-BF91-4CD0-BCD2-4793D9599E0A
ms.date: 06/23/2022
ms.keywords: GetFrameStatistics, GetFrameStatistics method [DirectComposition], GetFrameStatistics method [DirectComposition],IDCompositionDevice interface, IDCompositionDevice interface [DirectComposition],GetFrameStatistics method, IDCompositionDevice.GetFrameStatistics, IDCompositionDevice::GetFrameStatistics, dcomp/IDCompositionDevice::GetFrameStatistics, directcomp.idcompositiondevice_getframestatistics
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
 - IDCompositionDevice::GetFrameStatistics
 - dcomp/IDCompositionDevice::GetFrameStatistics
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
 - IDCompositionDevice.GetFrameStatistics
---

# IDCompositionDevice::GetFrameStatistics


## -description

Retrieves information from the composition engine about composition times and the frame rate.

## -parameters

### -param statistics [out]

Type: <b><a href="/windows/desktop/api/dcomptypes/ns-dcomptypes-dcomposition_frame_statistics">DCOMPOSITION_FRAME_STATISTICS</a>*</b>

A structure that receives composition times and frame rate information.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.

## -remarks

This method retrieves timing information about the composition engine that an application can use to synchronize the rasterization of bitmaps with independent animations.

## -see-also

<a href="/windows/desktop/directcomp/basic-concepts">Composition Target Window</a>



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice">IDCompositionDevice</a>