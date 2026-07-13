---
UID: NF:dcomp.DCompositionBoostCompositorClock
tech.root: directcomp
title: DCompositionBoostCompositorClock
ms.date: 06/24/2021
targetos: Windows
description: Requests that the system dynamically switch to a higher refresh rate to enhance latency-sensitive content.
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
 - HeaderDef
api_location:
 - dcomp.h
api_name:
 - DCompositionBoostCompositorClock
f1_keywords:
 - DCompositionBoostCompositorClock
 - dcomp/DCompositionBoostCompositorClock
dev_langs:
 - c++
---

## -description

Requests that the system dynamically switch to a higher refresh rate to enhance latency-sensitive content.

## -parameters

### -param enable

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`TRUE` to request that the system dynamically switch to a higher refresh rate; otherwise, `FALSE`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

[DCompositionGetTargetStatistics](/windows/win32/api/dcomp/nf-dcomp-dcompositiongetstatistics), [DCompositionGetStatistics](nf-dcomp-dcompositiongetstatistics.md), [DCompositionGetFrameId](nf-dcomp-dcompositiongetframeid.md), [DCompositionWaitForCompositorClock](nf-dcomp-dcompositionwaitforcompositorclock.md)
