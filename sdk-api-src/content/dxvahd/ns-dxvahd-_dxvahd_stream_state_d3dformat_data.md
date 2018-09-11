---
UID: NS:dxvahd._DXVAHD_STREAM_STATE_D3DFORMAT_DATA
title: "_DXVAHD_STREAM_STATE_D3DFORMAT_DATA"
author: windows-sdk-content
description: Specifies the format for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_stream_state_d3dformat_data.htm
tech.root: medfound
ms.assetid: a1ba825b-0574-4657-8a10-447a3caf8149
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: DXVAHD_STREAM_STATE_D3DFORMAT_DATA, DXVAHD_STREAM_STATE_D3DFORMAT_DATA structure [Media Foundation], _DXVAHD_STREAM_STATE_D3DFORMAT_DATA, dxvahd/DXVAHD_STREAM_STATE_D3DFORMAT_DATA, mf.dxvahd_stream_state_d3dformat_data
ms.prod: windows
ms.technology: windows-sdk
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
 - DXVAHD_STREAM_STATE_D3DFORMAT_DATA
product: Windows
targetos: Windows
req.typenames: DXVAHD_STREAM_STATE_D3DFORMAT_DATA
req.redist: 
---

# _DXVAHD_STREAM_STATE_D3DFORMAT_DATA structure


## -description


Specifies the format for an input stream, when using Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field Format

The surface format, specified as a <b>D3DFORMAT</b> value. You can also use a FOURCC code to specify a format that is not defined in the <b>D3DFORMAT</b> enumeration. For more information, see <a href="https://msdn.microsoft.com/bea4835d-fd7f-4ac3-8466-7f4e0d799a12">Video FOURCCs</a>.

The default state value is <b>D3DFMT_UNKNOWN</b>.


## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

