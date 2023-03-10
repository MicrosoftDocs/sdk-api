---
UID: NE:dxgi1_6.DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS
title: DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS (dxgi1_6.h)
description: Describes which levels of hardware composition are supported.
helpviewer_keywords: ["DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS","DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS enumeration [DXGI]","DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_CURSOR_STRETCHED","DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_FULLSCREEN","DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_WINDOWED","direct3ddxgi.dxgi_hardware_composition_support_flags","dxgi1_6/DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS","dxgi1_6/DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_CURSOR_STRETCHED","dxgi1_6/DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_FULLSCREEN","dxgi1_6/DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_WINDOWED"]
old-location: direct3ddxgi\dxgi_hardware_composition_support_flags.htm
tech.root: direct3ddxgi
ms.assetid: FA8BCF74-58CB-4806-A0A5-1D8E6EC576DC
ms.date: 12/05/2018
ms.keywords: DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS, DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS enumeration [DXGI], DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_CURSOR_STRETCHED, DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_FULLSCREEN, DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_WINDOWED, direct3ddxgi.dxgi_hardware_composition_support_flags, dxgi1_6/DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS, dxgi1_6/DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_CURSOR_STRETCHED, dxgi1_6/DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_FULLSCREEN, dxgi1_6/DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_WINDOWED
req.header: dxgi1_6.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS
 - dxgi1_6/DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgi1_6.h
api_name:
 - DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS
---

# DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAGS enumeration


## -description

Describes which levels of hardware composition are supported.

## -enum-fields

### -field DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_FULLSCREEN:1

This flag specifies that swapchain composition can be facilitated in a performant manner using hardware for fullscreen applications.

### -field DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_WINDOWED:2

This flag specifies that swapchain composition can be facilitated in a performant manner using hardware for windowed applications.

### -field DXGI_HARDWARE_COMPOSITION_SUPPORT_FLAG_CURSOR_STRETCHED:4

This flag specifies that swapchain composition facilitated using hardware can cause the cursor to appear stretched.

## -remarks

Values of this enumeration are returned from the <a href="/windows/desktop/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport">IDXGIOutput6::CheckHardwareCompositionSupport</a> method in the <i>pFlags</i> out parameter.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-enums">DXGI Enumerations</a>



<a href="/windows/desktop/api/dxgi1_6/nf-dxgi1_6-idxgioutput6-checkhardwarecompositionsupport">IDXGIOutput6::CheckHardwareCompositionSupport method</a>
