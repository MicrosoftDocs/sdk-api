---
UID: NF:presentation.CreatePresentationFactory
tech.root: comp_swapchain
title: CreatePresentationFactory
ms.date: 06/08/2021
targetos: Windows
description: Creates a presentation factory.
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
 - DllExport
api_location:
 - dcomp.dll
api_name:
 - CreatePresentationFactory
f1_keywords:
 - CreatePresentationFactory
 - presentation/CreatePresentationFactory
dev_langs:
 - c++
---

## -description

Creates a presentation factory.

## -parameters

### -param d3dDevice

Type: **[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\***

The D3D device the presentation factory is bound to.

### -param riid

Type: **REFIID**

A reference to the interface identifier (IID) of the presentation factory.

### -param presentationFactory

Type: **[void](/windows/desktop/winprog/windows-data-types)\*\***

The address of a pointer to an interface with the IID specified in the *riid* parameter.

## -returns

## -remarks

## -see-also

