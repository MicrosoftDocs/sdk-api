---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# __MIDL___MIDL_itf_vmr9_0000_0006_0001 enumeration


## -description



The <b>VMR9AlphaBitmapFlags</b> enumeration type defines the possible values for the <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/62214c24-0a4b-43c3-91dc-3eb6e5df3d94">VMR9AlphaBitmap</a> structure.




## -enum-fields




### -field VMR9AlphaBitmap_Disable


            Disable the alpha bitmap. This flag cannot be combined with any other flags.
          


### -field VMR9AlphaBitmap_hDC


            The bitmap is specified as a GDI device context (HDC) in the <b>hdc</b> member of the <a href="https://msdn.microsoft.com/62214c24-0a4b-43c3-91dc-3eb6e5df3d94">VMR9AlphaBitmap</a> structure. If this flag is not present, the bitmap is specified as a Direct3D <b>IDirect3DSurface9</b> pointer in the <b>pDDS</b> member of the structure.
          


### -field VMR9AlphaBitmap_EntireDDS


            Use the entire Direct3D surface. The <b>rSrc</b> member of the <a href="https://msdn.microsoft.com/62214c24-0a4b-43c3-91dc-3eb6e5df3d94">VMR9AlphaBitmap</a> structure is ignored. This flag cannot be combined with the VMR9AlphaBitmap_hDC flag.
          


### -field VMR9AlphaBitmap_SrcColorKey


            Indicates that the <b>srcClrKey</b> member is valid and should be used when blending. This flag cannot be used with a Direct3D surface that contains per-pixel alpha (D3DFMT_A8R8G8B8 format).
          


### -field VMR9AlphaBitmap_SrcRect


            Indicates that the <b>rSrc</b> member is valid and specifies a sub-rectangle of the original image to be blended. This flag is only valid for the <a href="https://msdn.microsoft.com/89aa0212-9311-4f23-9f55-7e7a1072a19a">IVMRMixerBitmap9::UpdateAlphaBitmapParameters</a> method.
          


### -field VMR9AlphaBitmap_FilterMode


            Indicates that the <b>dwFilterMode</b> member is valid and should be used to overide the VMR filter's default filtering method.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

