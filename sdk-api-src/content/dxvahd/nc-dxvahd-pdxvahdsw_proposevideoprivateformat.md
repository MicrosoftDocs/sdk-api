---
UID: NC:dxvahd.PDXVAHDSW_ProposeVideoPrivateFormat
title: PDXVAHDSW_ProposeVideoPrivateFormat (dxvahd.h)
description: Gets a private surface format from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["PDXVAHDSW_ProposeVideoPrivateFormat","PDXVAHDSW_ProposeVideoPrivateFormat callback","PDXVAHDSW_ProposeVideoPrivateFormat callback function [Media Foundation]","dxvahd/PDXVAHDSW_ProposeVideoPrivateFormat","mf.pdxvahdsw_proposevideoprivateformat"]
old-location: mf\pdxvahdsw_proposevideoprivateformat.htm
tech.root: mf
ms.assetid: b543f05f-40fc-4bdf-ae53-9a451d3bdf2a
ms.date: 12/05/2018
ms.keywords: PDXVAHDSW_ProposeVideoPrivateFormat, PDXVAHDSW_ProposeVideoPrivateFormat callback, PDXVAHDSW_ProposeVideoPrivateFormat callback function [Media Foundation], dxvahd/PDXVAHDSW_ProposeVideoPrivateFormat, mf.pdxvahdsw_proposevideoprivateformat
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDXVAHDSW_ProposeVideoPrivateFormat
 - dxvahd/PDXVAHDSW_ProposeVideoPrivateFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - dxvahd.h
api_name:
 - PDXVAHDSW_ProposeVideoPrivateFormat
---

# PDXVAHDSW_ProposeVideoPrivateFormat callback function


## -description

Gets a private surface format from a software plug-in Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -parameters

### -param hDevice [in]

A handle to the plug-in DXVA-HD device.

### -param pFormat [in, out]

A pointer to a <b>D3DFORMAT</b> value. On input, specifies the surface format that is requested by the application. On output, specifies the private surface format that the plug-in device proposes.

## -returns

If this callback function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This function is called when the application calls <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface">IDXVAHD_Device::CreateVideoSurface</a>  if  the following conditions are true:

<ul>
<li>The type of input surface is <b>DXVAHD_SURFACE_TYPE_VIDEO_INPUT_PRIVATE</b>.</li>
<li>The Direct3D device does not support the surface format requested by the application natively.</li>
</ul>
This function enables the plug-in device to propose an alternate format with an equivalent memory layout. For example, if the application requests AYUV, the plug-in device might allocate a surface of type <b>D3DFMT_A8R8G8B8</b>.

If the function succeeds, the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface">CreateVideoSurface</a> method attempts to create a surface with the format returned in <i>pFormat</i>. 


#### Examples

The following code shows how a plug-in device proposes <b>D3DFMT_A8R8G8B8</b> as an alternative surface format for AYUV. 


```
HRESULT CALLBACK ProposeVideoPrivateFormat(
    HANDLE hDevice,
    D3DFORMAT* pFormat 
    )
{
    switch (*pFormat)
    {
        case D3DFMT_AYUV: 
            *pFormat = D3DFMT_A8R8G8B8; 
            return S_OK;

        default: 
            return E_FAIL;
    }
}

```

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahdsw_callbacks">DXVAHDSW_CALLBACKS</a>



<a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface">IDXVAHD_Device::CreateVideoSurface</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>
