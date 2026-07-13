---
UID: NF:presentation.IPresentationFactory.CreatePresentationManager
tech.root: comp_swapchain
title: IPresentationFactory::CreatePresentationManager
ms.date: 06/08/2021
targetos: Windows
description: Creates a presentation manager.
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
 - IPresentationFactory::CreatePresentationManager
f1_keywords:
 - IPresentationFactory::CreatePresentationManager
 - presentation/IPresentationFactory::CreatePresentationManager
dev_langs:
 - c++
---

## -description

Creates a presentation manager.

## -parameters

### -param ppPresentationManager

Type: **[IPresentationManager](nn-presentation-ipresentationmanager.md) \*\***

The address of a pointer to the created presentation manager.

## -returns

Type: **[HRESULT](/windows/desktop/winprog/windows-data-types)**

If the function succeeds, it returns `S_OK`; otherwise, it returns an `HRESULT` value that indicates the error.

## -remarks

## -see-also

