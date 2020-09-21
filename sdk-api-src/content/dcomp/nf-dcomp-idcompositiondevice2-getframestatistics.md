---
UID: NF:dcomp.IDCompositionDevice2.GetFrameStatistics
title: IDCompositionDevice2::GetFrameStatistics (dcomp.h)
description: Retrieves information from the composition engine about composition times and the frame rate.
helpviewer_keywords: ["GetFrameStatistics","GetFrameStatistics method [DirectComposition]","GetFrameStatistics method [DirectComposition]","IDCompositionDevice2 interface","IDCompositionDevice2 interface [DirectComposition]","GetFrameStatistics method","IDCompositionDevice2.GetFrameStatistics","IDCompositionDevice2::GetFrameStatistics","dcomp/IDCompositionDevice2::GetFrameStatistics","directcomp.idcompositiondevice2_getframestatistics"]
old-location: directcomp\idcompositiondevice2_getframestatistics.htm
tech.root: directcomp
ms.assetid: 5C529575-46AC-495A-9165-15FC8F6B1F69
ms.date: 12/05/2018
ms.keywords: GetFrameStatistics, GetFrameStatistics method [DirectComposition], GetFrameStatistics method [DirectComposition],IDCompositionDevice2 interface, IDCompositionDevice2 interface [DirectComposition],GetFrameStatistics method, IDCompositionDevice2.GetFrameStatistics, IDCompositionDevice2::GetFrameStatistics, dcomp/IDCompositionDevice2::GetFrameStatistics, directcomp.idcompositiondevice2_getframestatistics
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - IDCompositionDevice2::GetFrameStatistics
 - dcomp/IDCompositionDevice2::GetFrameStatistics
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
 - IDCompositionDevice2.GetFrameStatistics
---

# IDCompositionDevice2::GetFrameStatistics


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



<a href="/windows/desktop/api/dcomp/nn-dcomp-idcompositiondevice2">IDCompositionDevice2</a>