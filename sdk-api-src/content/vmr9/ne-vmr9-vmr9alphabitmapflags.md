---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0006_0001
title: VMR9AlphaBitmapFlags (vmr9.h)
description: The VMR9AlphaBitmapFlags enumeration type defines the possible values for the dwFlags member of the VMR9AlphaBitmap structure.
helpviewer_keywords: ["VMR9AlphaBitmapFlags","VMR9AlphaBitmapFlags","VMR9AlphaBitmapFlags enumeration [DirectShow]","VMR9AlphaBitmapFlagsEnumeration","VMR9AlphaBitmap_Disable","VMR9AlphaBitmap_EntireDDS","VMR9AlphaBitmap_FilterMode","VMR9AlphaBitmap_SrcColorKey","VMR9AlphaBitmap_SrcRect","VMR9AlphaBitmap_hDC","dshow.vmr9alphabitmapflags","vmr9/VMR9AlphaBitmapFlags","vmr9/VMR9AlphaBitmap_Disable","vmr9/VMR9AlphaBitmap_EntireDDS","vmr9/VMR9AlphaBitmap_FilterMode","vmr9/VMR9AlphaBitmap_SrcColorKey","vmr9/VMR9AlphaBitmap_SrcRect","vmr9/VMR9AlphaBitmap_hDC"]
old-location: dshow\vmr9alphabitmapflags.htm
tech.root: dshow
ms.assetid: 0b36dd8c-02c6-41f4-a916-205f2c74ea46
ms.date: 12/05/2018
ms.keywords: VMR9AlphaBitmapFlags, VMR9AlphaBitmapFlags , VMR9AlphaBitmapFlags enumeration [DirectShow], VMR9AlphaBitmapFlagsEnumeration, VMR9AlphaBitmap_Disable, VMR9AlphaBitmap_EntireDDS, VMR9AlphaBitmap_FilterMode, VMR9AlphaBitmap_SrcColorKey, VMR9AlphaBitmap_SrcRect, VMR9AlphaBitmap_hDC, dshow.vmr9alphabitmapflags, vmr9/VMR9AlphaBitmapFlags, vmr9/VMR9AlphaBitmap_Disable, vmr9/VMR9AlphaBitmap_EntireDDS, vmr9/VMR9AlphaBitmap_FilterMode, vmr9/VMR9AlphaBitmap_SrcColorKey, vmr9/VMR9AlphaBitmap_SrcRect, vmr9/VMR9AlphaBitmap_hDC
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
req.typenames: VMR9AlphaBitmapFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_vmr9_0000_0006_0001
 - vmr9/__MIDL___MIDL_itf_vmr9_0000_0006_0001
 - VMR9AlphaBitmapFlags
 - vmr9/VMR9AlphaBitmapFlags
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
 - VMR9AlphaBitmapFlags
---

# VMR9AlphaBitmapFlags enumeration


## -description

The <b>VMR9AlphaBitmapFlags</b> enumeration type defines the possible values for the <b>dwFlags</b> member of the <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9alphabitmap">VMR9AlphaBitmap</a> structure.

## -enum-fields

### -field VMR9AlphaBitmap_Disable:0x1

Disable the alpha bitmap. This flag cannot be combined with any other flags.

### -field VMR9AlphaBitmap_hDC:0x2

The bitmap is specified as a GDI device context (HDC) in the <b>hdc</b> member of the <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9alphabitmap">VMR9AlphaBitmap</a> structure. If this flag is not present, the bitmap is specified as a Direct3D <b>IDirect3DSurface9</b> pointer in the <b>pDDS</b> member of the structure.

### -field VMR9AlphaBitmap_EntireDDS:0x4

Use the entire Direct3D surface. The <b>rSrc</b> member of the <a href="/previous-versions/windows/desktop/api/vmr9/ns-vmr9-vmr9alphabitmap">VMR9AlphaBitmap</a> structure is ignored. This flag cannot be combined with the VMR9AlphaBitmap_hDC flag.

### -field VMR9AlphaBitmap_SrcColorKey:0x8

Indicates that the <b>srcClrKey</b> member is valid and should be used when blending. This flag cannot be used with a Direct3D surface that contains per-pixel alpha (D3DFMT_A8R8G8B8 format).

### -field VMR9AlphaBitmap_SrcRect:0x10

Indicates that the <b>rSrc</b> member is valid and specifies a sub-rectangle of the original image to be blended. This flag is only valid for the <a href="/windows/desktop/api/vmr9/nf-vmr9-ivmrmixerbitmap9-updatealphabitmapparameters">IVMRMixerBitmap9::UpdateAlphaBitmapParameters</a> method.

### -field VMR9AlphaBitmap_FilterMode:0x20

Indicates that the <b>dwFilterMode</b> member is valid and should be used to override the VMR filter's default filtering method.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
