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

# _DXVAHD_STREAM_STATE_PRIVATE_DATA structure


## -description


Contains data for a private stream state, for  a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) input stream. 


## -struct-fields




### -field Guid

A GUID that identifies the private stream state. The following GUID is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DXVAHD_STREAM_STATE_PRIVATE_IVTC"></a><a id="dxvahd_stream_state_private_ivtc"></a><dl>
<dt><b>DXVAHD_STREAM_STATE_PRIVATE_IVTC</b></dt>
</dl>
</td>
<td width="60%">
Retrieves statistics about inverse telecine. The state data (<b>pData</b>) is a <a href="https://msdn.microsoft.com/166fc57e-3b49-44c1-8c6c-691950e7b675">DXVAHD_STREAM_STATE_PRIVATE_IVTC_DATA</a> structure.

</td>
</tr>
</table>
 

A device can define additional GUIDs for use with custom stream states. The interpretation of the data is then defined by the device.


### -field DataSize

The size, in bytes, of the buffer pointed to by the <b>pData</b> member.


### -field pData

A pointer to a buffer that contains the private state data. The DXVA-HD runtime passes this buffer directly to the device, without validation.


## -remarks



Use this structure for proprietary or device-specific state parameters.

The caller allocates the <b>pData</b> array. Set the <b>DataSize</b> member to the size of the array in bytes. When retrieving the state data, you can set the <b>pData</b> member to <b>NULL</b> to get the size of the data. The device will return the size in the <b>DataSize</b> member.






## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/75036101-7498-4d66-afc3-df76ae3cca39">DXVAHD_STREAM_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/40a8444f-576e-40ff-804e-0912812f0ee6">IDXVAHD_VideoProcessor::SetVideoProcessStreamState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

