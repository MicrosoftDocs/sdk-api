---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0006_0001
title: VMR9AlphaBitmapFlags (vmr9.h)
author: windows-sdk-content
description: The VMR9AlphaBitmapFlags enumeration type defines the possible values for the dwFlags member of the VMR9AlphaBitmap structure.
old-location: dshow\vmr9alphabitmapflags.htm
tech.root: DirectShow
ms.assetid: 0b36dd8c-02c6-41f4-a916-205f2c74ea46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VMR9AlphaBitmapFlags, VMR9AlphaBitmapFlags , VMR9AlphaBitmapFlags enumeration [DirectShow], VMR9AlphaBitmapFlagsEnumeration, VMR9AlphaBitmap_Disable, VMR9AlphaBitmap_EntireDDS, VMR9AlphaBitmap_FilterMode, VMR9AlphaBitmap_SrcColorKey, VMR9AlphaBitmap_SrcRect, VMR9AlphaBitmap_hDC, dshow.vmr9alphabitmapflags, vmr9/VMR9AlphaBitmapFlags, vmr9/VMR9AlphaBitmap_Disable, vmr9/VMR9AlphaBitmap_EntireDDS, vmr9/VMR9AlphaBitmap_FilterMode, vmr9/VMR9AlphaBitmap_SrcColorKey, vmr9/VMR9AlphaBitmap_SrcRect, vmr9/VMR9AlphaBitmap_hDC
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vmr9.h
api_name:
 - VMR9AlphaBitmapFlags
product: Windows
targetos: Windows
req.typenames: VMR9AlphaBitmapFlags
req.redist: 
ms.custom: 19H1
---

# VMR9AlphaBitmapFlags enumeration


## -description



The <b>VMR9AlphaBitmapFlags</b> enumeration type defines the possible values for the <b>dwFlags</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/ns-vmr9-_vmr9alphabitmap">VMR9AlphaBitmap</a> structure.




## -enum-fields




### -field VMR9AlphaBitmap_Disable

Disable the alpha bitmap. This flag cannot be combined with any other flags.
          


### -field VMR9AlphaBitmap_hDC

The bitmap is specified as a GDI device context (HDC) in the <b>hdc</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/ns-vmr9-_vmr9alphabitmap">VMR9AlphaBitmap</a> structure. If this flag is not present, the bitmap is specified as a Direct3D <b>IDirect3DSurface9</b> pointer in the <b>pDDS</b> member of the structure.
          


### -field VMR9AlphaBitmap_EntireDDS

Use the entire Direct3D surface. The <b>rSrc</b> member of the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/ns-vmr9-_vmr9alphabitmap">VMR9AlphaBitmap</a> structure is ignored. This flag cannot be combined with the VMR9AlphaBitmap_hDC flag.
          


### -field VMR9AlphaBitmap_SrcColorKey

Indicates that the <b>srcClrKey</b> member is valid and should be used when blending. This flag cannot be used with a Direct3D surface that contains per-pixel alpha (D3DFMT_A8R8G8B8 format).
          


### -field VMR9AlphaBitmap_SrcRect

Indicates that the <b>rSrc</b> member is valid and specifies a sub-rectangle of the original image to be blended. This flag is only valid for the <a href="https://docs.microsoft.com/windows/desktop/api/vmr9/nf-vmr9-ivmrmixerbitmap9-updatealphabitmapparameters">IVMRMixerBitmap9::UpdateAlphaBitmapParameters</a> method.
          


### -field VMR9AlphaBitmap_FilterMode

Indicates that the <b>dwFilterMode</b> member is valid and should be used to overide the VMR filter's default filtering method.
          


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-enumerated-types">DirectShow Enumerated Types</a>
 

 

