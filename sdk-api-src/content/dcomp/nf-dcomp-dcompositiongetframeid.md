---
UID: NF:dcomp.DCompositionGetFrameId
tech.root: directcomp
title: DCompositionGetFrameId
ms.date: 06/24/2021
targetos: Windows
description: Gets the identifier of the most recent compositor frame of the specified type.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: dcomp.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: dcomp.lib
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows Build 22000
req.target-min-winversvr: Windows Build 22000
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - DllExport
api_location:
 - dcomp.dll
api_name:
 - DCompositionGetFrameId
f1_keywords:
 - DCompositionGetFrameId
 - dcomp/DCompositionGetFrameId
dev_langs:
 - c++
---

## -description

Gets the identifier of the most recent compositor frame of the specified type.

## -parameters

### -param frameIdType

Type: **[COMPOSITION_FRAME_ID_TYPE](../dcomptypes/ne-dcomptypes-composition_frame_id_type.md)**

The type of the compositor frame.

### -param frameId

Type: **COMPOSITION_FRAME_ID\***

The identifer of the most recent compositor frame of the specified type.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

[DCompositionGetTargetStatistics](https://github.com/MicrosoftDocs/sdk-api/blob/docs/sdk-api-src/content/dcomp/nf-dcomp-dcompositiongettargetstatistics.md), [DCompositionGetStatistics](nf-dcomp-dcompositiongetstatistics.md), [DCompositionBoostCompositorClock](nf-dcomp-dcompositionboostcompositorclock.md), [DCompositionWaitForCompositorClock](nf-dcomp-dcompositionwaitforcompositorclock.md)
