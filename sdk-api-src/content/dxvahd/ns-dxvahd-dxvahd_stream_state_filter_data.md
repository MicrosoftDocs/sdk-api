---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_FILTER_DATA
title: DXVAHD_STREAM_STATE_FILTER_DATA (dxvahd.h)
author: windows-sdk-content
description: Specifies the level for a filtering operation on a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream.
old-location: mf\dxvahd_stream_state_filter_data.htm
tech.root: medfound
ms.assetid: 2f70222d-f87a-49a5-8da5-15dfa2807cd7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXVAHD_STREAM_STATE_FILTER_DATA, DXVAHD_STREAM_STATE_FILTER_DATA structure [Media Foundation], dxvahd/DXVAHD_STREAM_STATE_FILTER_DATA, mf.dxvahd_stream_state_filter_data
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHD_STREAM_STATE_FILTER_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_FILTER_DATA
req.redist: 
---

# DXVAHD_STREAM_STATE_FILTER_DATA structure


## -description


Specifies the level for a filtering operation on a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream.


## -struct-fields




### -field Enable

<b>If TRUE</b>, the filter is enabled. Otherwise, <b>the filter is disabled</b>.


### -field Level

The level for the filter. The meaning of this value depends on the implementation. To get the range and default value of a particular filter, call the <a href="https://msdn.microsoft.com/cff587a5-04ed-4f3e-bd05-0cb8d83fffb7">IDXVAHD_Device::GetVideoProcessorFilterRange</a> method.

If the <b>Enable</b> member is <b>FALSE</b>, the <b>Level</b> member is ignored.




## -remarks



For a list of image filters that are defined for DXVA-HD, see <a href="https://msdn.microsoft.com/e6abac04-c8cb-4130-b48e-fb5d25794d62">DXVAHD_FILTER</a>. The device might not support every type of image filter. To find out whether the device supports a particular filter, call the <a href="https://msdn.microsoft.com/93acad97-feee-46a5-95bf-51e560f91057">IDXVAHD_Device::GetVideoProcessorDeviceCaps</a> method and check the <b>FilterCaps</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure.


#### Examples


```cpp
HRESULT DXVAHD_SetFilterValue(
    IDXVAHD_VideoProcessor *pVP,
    UINT stream,
    DXVAHD_FILTER filter,
    BOOL bEnable,
    INT value
    )
{
    DXVAHD_STREAM_STATE_FILTER_DATA data = { bEnable, value };

    DXVAHD_STREAM_STATE state = static_cast<DXVAHD_STREAM_STATE>(DXVAHD_STREAM_STATE_FILTER_BRIGHTNESS + filter);

    HRESULT hr = pVP->SetVideoProcessStreamState(
        stream,
        state,
        sizeof(data),
        &data
        );

    return hr;
}

```





## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

