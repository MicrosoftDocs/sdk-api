---
UID: NS:dcomptypes.DCOMPOSITION_FRAME_STATISTICS
title: DCOMPOSITION_FRAME_STATISTICS (dcomptypes.h)
description: Describes timing and composition statistics for a frame.
helpviewer_keywords: ["DCOMPOSITION_FRAME_STATISTICS","DCOMPOSITION_FRAME_STATISTICS structure [DirectComposition]","PDCOMPOSITION_FRAME_STATISTICS","PDCOMPOSITION_FRAME_STATISTICS structure pointer [DirectComposition]","dcomptypes/DCOMPOSITION_FRAME_STATISTICS","dcomptypes/PDCOMPOSITION_FRAME_STATISTICS","directcomp.dcomposition_frame_statistics"]
old-location: directcomp\dcomposition_frame_statistics.htm
tech.root: directcomp
ms.assetid: 431D8399-9BCC-4B3A-89F4-E698446EF764
ms.date: 12/05/2018
ms.keywords: DCOMPOSITION_FRAME_STATISTICS, DCOMPOSITION_FRAME_STATISTICS structure [DirectComposition], PDCOMPOSITION_FRAME_STATISTICS, PDCOMPOSITION_FRAME_STATISTICS structure pointer [DirectComposition], dcomptypes/DCOMPOSITION_FRAME_STATISTICS, dcomptypes/PDCOMPOSITION_FRAME_STATISTICS, directcomp.dcomposition_frame_statistics
req.header: dcomptypes.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DCOMPOSITION_FRAME_STATISTICS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DCOMPOSITION_FRAME_STATISTICS
 - dcomptypes/DCOMPOSITION_FRAME_STATISTICS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DcompTypes.h
api_name:
 - DCOMPOSITION_FRAME_STATISTICS
---

# DCOMPOSITION_FRAME_STATISTICS structure


## -description

Describes timing and composition statistics for a frame.

## -struct-fields

### -field lastFrameTime

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a></b>

The time stamp of the last batch of commands to be processed by the composition engine.

### -field currentCompositionRate

Type: <b><a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a></b>

The rate at which the composition engine is producing frames, in frames per second.

### -field currentTime

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a></b>

The current time as computed by the <a href="/windows/desktop/api/profileapi/nf-profileapi-queryperformancecounter">QueryPerformanceCounter</a> function.

### -field timeFrequency

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a></b>

The units in which the <b>lastFrameTime</b> and <b>currentTime</b> members are specified, in Hertz.

### -field nextEstimatedFrameTime

Type: <b><a href="/windows/win32/api/winnt/ns-winnt-large_integer-r1">LARGE_INTEGER</a></b>

The estimated time when the next frame will be displayed.

## -remarks

The <a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-getframestatistics">IDCompositionDevice::GetFrameStatistics</a> method fills this structure. An application can use the information in this structure to estimate the timestamp of the next few frames that will be started by the composition engine. Note that this is only an estimate because the composition engine may or may not compose the next frame, depending on whether any active animations or other work are pending for that frame. In addition, the composition engine may change frame rates according to the cost of composing individual frames.

## -see-also

<a href="/windows/desktop/api/dcomp/nf-dcomp-idcompositiondevice-getframestatistics">IDCompositionDevice::GetFrameStatistics</a>

