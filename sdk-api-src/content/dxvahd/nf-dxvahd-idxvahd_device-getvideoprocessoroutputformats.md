---
UID: NF:dxvahd.IDXVAHD_Device.GetVideoProcessorOutputFormats
title: IDXVAHD_Device::GetVideoProcessorOutputFormats (dxvahd.h)
description: Gets a list of the output formats supported by the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.
helpviewer_keywords: ["GetVideoProcessorOutputFormats","GetVideoProcessorOutputFormats method [Media Foundation]","GetVideoProcessorOutputFormats method [Media Foundation]","IDXVAHD_Device interface","IDXVAHD_Device interface [Media Foundation]","GetVideoProcessorOutputFormats method","IDXVAHD_Device.GetVideoProcessorOutputFormats","IDXVAHD_Device::GetVideoProcessorOutputFormats","dxvahd/IDXVAHD_Device::GetVideoProcessorOutputFormats","mf.idxvahd_device_getvideoprocessoroutputformats"]
old-location: mf\idxvahd_device_getvideoprocessoroutputformats.htm
tech.root: mf
ms.assetid: e701014d-c112-42fa-9bf5-88cb31424006
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorOutputFormats, GetVideoProcessorOutputFormats method [Media Foundation], GetVideoProcessorOutputFormats method [Media Foundation],IDXVAHD_Device interface, IDXVAHD_Device interface [Media Foundation],GetVideoProcessorOutputFormats method, IDXVAHD_Device.GetVideoProcessorOutputFormats, IDXVAHD_Device::GetVideoProcessorOutputFormats, dxvahd/IDXVAHD_Device::GetVideoProcessorOutputFormats, mf.idxvahd_device_getvideoprocessoroutputformats
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
 - IDXVAHD_Device::GetVideoProcessorOutputFormats
 - dxvahd/IDXVAHD_Device::GetVideoProcessorOutputFormats
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_Device.GetVideoProcessorOutputFormats
---

# IDXVAHD_Device::GetVideoProcessorOutputFormats


## -description

Gets a list of the output formats supported by the Microsoft DirectX Video Acceleration High Definition (DXVA-HD) device.

## -parameters

### -param Count [in]

The number of formats to retrieve. This parameter must equal the <b>OutputFormatCount</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. Call the <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-getvideoprocessordevicecaps">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method to get this value.

### -param pFormats [out]

A pointer to an array of <b>D3DFORMAT</b> values. The <i>Count</i> parameter specifies the number of elements in the array. The method fills the array with a list of output formats.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The list of formats can include both <b>D3DFORMAT</b> values, such as <b>D3DFMT_X8R8G8B8</b>, and FOURCC codes, such as 'NV12'. For more information, see <a href="/windows/desktop/medfound/video-fourccs">Video FOURCCs</a>.
      


#### Examples


```cpp
// Checks whether a DXVA-HD device supports a specified output format.

HRESULT CheckOutputFormatSupport(
    IDXVAHD_Device          *pDXVAHD,
    const DXVAHD_VPDEVCAPS& caps,
    D3DFORMAT               d3dformat
    )
{
    D3DFORMAT *pFormats = new (std::nothrow) D3DFORMAT[caps.OutputFormatCount];
    if (pFormats == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pDXVAHD->GetVideoProcessorOutputFormats(
        caps.OutputFormatCount, 
        pFormats
        );

    if (FAILED(hr)) 
    { 
        goto done; 
    }

    UINT index;
    for (index = 0; index < caps.OutputFormatCount; index++)
    {
        if (pFormats[index] == d3dformat)
        {
            break;
        }
    }
    if (index == caps.OutputFormatCount)
    {
        hr = E_FAIL;
    }

done:
    delete [] pFormats;
    return hr;
}

```

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_device">IDXVAHD_Device</a>