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

# IDXVAHD_Device::CreateVideoSurface


## -description


Creates one or more Microsoft Direct3D video surfaces.


## -parameters




### -param Width [in]

The width of each surface, in pixels.


### -param Height [in]

The height of each surface, in pixels.


### -param Format [in]

The pixel format, specified as a <b>D3DFORMAT</b> value or FOURCC code. For more information, see <a href="https://msdn.microsoft.com/bea4835d-fd7f-4ac3-8466-7f4e0d799a12">Video FOURCCs</a>.


### -param Pool [in]

The memory pool in which the surface is  created. This parameter must equal the <b>InputPool</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure. Call the <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method to get this value.


### -param Usage [in]

Reserved. Set to 0.


### -param Type [in]

The type of surface to create, specified as a member of the <a href="https://msdn.microsoft.com/06df2d2f-9163-4672-8ea4-57f1942320c5">DXVAHD_SURFACE_TYPE</a> enumeration.


### -param NumSurfaces [in]

The number of surfaces to create.


### -param ppSurfaces [out]

A pointer to an array of <b>IDirect3DSurface9</b> pointers. The <i>NumSurfaces</i> parameter specifies the number of elements in the array. The method fills the array with pointers to the new video surfaces. The caller must release the pointers.


### -param pSharedHandle [in, out]

Reserved. Set to <b>NULL</b>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/3f79ac9c-2aed-4e1c-bf6f-02f9c54d59cd">IDXVAHD_Device</a>
 

 

