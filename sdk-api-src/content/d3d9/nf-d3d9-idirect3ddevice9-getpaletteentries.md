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

# IDirect3DDevice9::GetPaletteEntries


## -description


Retrieves palette entries.


## -parameters




### -param PaletteNumber [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

An ordinal value identifying the particular palette to retrieve. 


### -param pEntries [in, out]

Type: <b><a href="https://msdn.microsoft.com/8ee46b54-e076-4b85-a55e-a7974a4c58b6">PALETTEENTRY</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/8ee46b54-e076-4b85-a55e-a7974a4c58b6">PALETTEENTRY</a> structure, representing the returned palette entries. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If the method succeeds, the return value is D3D_OK. If the method fails, the return value can be D3DERR_INVALIDCALL.




## -remarks



For more information about <a href="https://msdn.microsoft.com/8ee46b54-e076-4b85-a55e-a7974a4c58b6">PALETTEENTRY</a>, see the Platform SDK.

<div class="alert"><b>Note</b>  As of Direct3D 9, the peFlags member of the <a href="https://msdn.microsoft.com/8ee46b54-e076-4b85-a55e-a7974a4c58b6">PALETTEENTRY</a> structure does not work the way it is documented in the Platform SDK. The peFlags member is now the alpha channel for 8-bit palettized formats.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/cf951e8e-7adb-417a-bda0-9b3cde4912a7">IDirect3DDevice9</a>



<a href="https://msdn.microsoft.com/e72ec7a1-9904-4a07-a662-24c6532cfdc8">IDirect3DDevice9::GetCurrentTexturePalette</a>



<a href="https://msdn.microsoft.com/5d97ccf4-20cd-4773-905a-e12b279e4f0b">IDirect3DDevice9::SetCurrentTexturePalette</a>



<a href="https://msdn.microsoft.com/7b205c4a-b01c-4856-91de-d45645f38404">IDirect3DDevice9::SetPaletteEntries</a>



<a href="https://msdn.microsoft.com/dea4b4bc-7eba-40fa-9c2c-0851fe7e231b">Texture Palettes (Direct3D 9)</a>
 

 

