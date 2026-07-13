---
UID: NF:presentation.IPresentationManager.EnablePresentStatisticsKind
tech.root: comp_swapchain
title: IPresentationManager::EnablePresentStatisticsKind
ms.date: 06/08/2021
targetos: Windows
description: Enables or disables the specified present statistics kind.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: dcomp.dll
req.header: presentation.h
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
 - COM
api_location:
 - presentation.h
api_name:
 - IPresentationManager::EnablePresentStatisticsKind
f1_keywords:
 - IPresentationManager::EnablePresentStatisticsKind
 - presentation/IPresentationManager::EnablePresentStatisticsKind
dev_langs:
 - c++
---

## -description

Enables or disables the specified present statistics kind.

## -parameters

### -param presentStatisticsKind

Type: **[PresentStatisticsKind](../presentationtypes/ne-presentationtypes-presentstatisticskind.md)**

The present statistics kind to enable or disable.

### -param enabled

Type: **[BOOLEAN](/windows/win32/winprog/windows-data-types)**

`TRUE` to enable the present statistics kind; otherwise, `FALSE`.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

The requested change takes place as soon as possible, however effects can be delayed. We suggest that you register all desired present statistics before you issue presents, and not change during use. This is also how statistics can be extended and changed in the future without breaking backwards compatibility.

## -see-also

