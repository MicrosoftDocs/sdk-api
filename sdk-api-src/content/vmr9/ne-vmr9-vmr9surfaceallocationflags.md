---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0001_0001
title: VMR9SurfaceAllocationFlags (vmr9.h)
description: The VMR9SurfaceAllocationFlags enumeration type is used with the IVMRSurfaceAllocator9::InitializeDevice method to specify surface creation parameters (VMR-9 only).
helpviewer_keywords: ["VMR9AllocFlag_3DRenderTarget","VMR9AllocFlag_DXVATarget","VMR9AllocFlag_OffscreenSurface","VMR9AllocFlag_RGBDynamicSwitch","VMR9AllocFlag_TextureSurface","VMR9AllocFlag_UsageMask","VMR9AllocFlag_UsageReserved","VMR9SurfaceAllocationFlags","VMR9SurfaceAllocationFlags","VMR9SurfaceAllocationFlags enumeration [DirectShow]","VMR9SurfaceAllocationFlagsEnumeration","dshow.vmr9surfaceallocationflags","vmr9/VMR9AllocFlag_3DRenderTarget","vmr9/VMR9AllocFlag_DXVATarget","vmr9/VMR9AllocFlag_OffscreenSurface","vmr9/VMR9AllocFlag_RGBDynamicSwitch","vmr9/VMR9AllocFlag_TextureSurface","vmr9/VMR9AllocFlag_UsageMask","vmr9/VMR9AllocFlag_UsageReserved","vmr9/VMR9SurfaceAllocationFlags"]
old-location: dshow\vmr9surfaceallocationflags.htm
tech.root: dshow
ms.assetid: 880e6c78-177f-49d0-a526-5f036c715f9e
ms.date: 12/05/2018
ms.keywords: VMR9AllocFlag_3DRenderTarget, VMR9AllocFlag_DXVATarget, VMR9AllocFlag_OffscreenSurface, VMR9AllocFlag_RGBDynamicSwitch, VMR9AllocFlag_TextureSurface, VMR9AllocFlag_UsageMask, VMR9AllocFlag_UsageReserved, VMR9SurfaceAllocationFlags, VMR9SurfaceAllocationFlags , VMR9SurfaceAllocationFlags enumeration [DirectShow], VMR9SurfaceAllocationFlagsEnumeration, dshow.vmr9surfaceallocationflags, vmr9/VMR9AllocFlag_3DRenderTarget, vmr9/VMR9AllocFlag_DXVATarget, vmr9/VMR9AllocFlag_OffscreenSurface, vmr9/VMR9AllocFlag_RGBDynamicSwitch, vmr9/VMR9AllocFlag_TextureSurface, vmr9/VMR9AllocFlag_UsageMask, vmr9/VMR9AllocFlag_UsageReserved, vmr9/VMR9SurfaceAllocationFlags
req.header: vmr9.h
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
req.typenames: VMR9SurfaceAllocationFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_vmr9_0000_0001_0001
 - vmr9/__MIDL___MIDL_itf_vmr9_0000_0001_0001
 - VMR9SurfaceAllocationFlags
 - vmr9/VMR9SurfaceAllocationFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9SurfaceAllocationFlags
---

# VMR9SurfaceAllocationFlags enumeration


## -description

The <b>VMR9SurfaceAllocationFlags</b> enumeration type is used with the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice">IVMRSurfaceAllocator9::InitializeDevice</a> method to specify surface creation parameters (VMR-9 only).

## -enum-fields

### -field VMR9AllocFlag_3DRenderTarget:0x1

Indicates that the surface is a Direct3D render target.

### -field VMR9AllocFlag_DXVATarget:0x2

Indicates that the render target supports DXVA.

### -field VMR9AllocFlag_TextureSurface:0x4

Indicates that the target is a Direct3D texture surface.

### -field VMR9AllocFlag_OffscreenSurface:0x8

Indicates an offscreen surface.

### -field VMR9AllocFlag_RGBDynamicSwitch:0x10

In YUV mixing mode, indicates that the mixer can accept RGB formats in addition to the specified YUV format. The allocator-presenter can switch between the formats dynamically. This flag is only valid in YUV mixing mode.

### -field VMR9AllocFlag_UsageReserved:0xe0

Reserved for future use.

### -field VMR9AllocFlag_UsageMask:0xff

Bitwise <b>OR</b> of all flags; not used by applications

## -remarks

The VMR9AllocFlag_TextureSurface flag can be combined with the VMR9AllocFlag_DXVATarget and VMR9AllocFlag_3DRenderTarget flags.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
