---
UID: NS:dxvahd._DXVAHD_BLT_STATE_PRIVATE_DATA
title: "_DXVAHD_BLT_STATE_PRIVATE_DATA"
author: windows-sdk-content
description: Contains data for a private blit state for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahd_blt_state_private_data.htm
old-project: medfound
ms.assetid: b85d4429-9346-4c85-8c3d-efffe0c1e63a
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DXVAHD_BLT_STATE_PRIVATE_DATA, DXVAHD_BLT_STATE_PRIVATE_DATA structure [Media Foundation], _DXVAHD_BLT_STATE_PRIVATE_DATA, dxvahd/DXVAHD_BLT_STATE_PRIVATE_DATA, mf.dxvahd_blt_state_private_data
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
tech.root: 
req.typenames: DXVAHD_BLT_STATE_PRIVATE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	dxvahd.h
api_name:
-	DXVAHD_BLT_STATE_PRIVATE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# _DXVAHD_BLT_STATE_PRIVATE_DATA structure


## -description


Contains data for a private blit state for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field Guid

A GUID that identifies the private state. The meaning of this value is defined by the device.




### -field DataSize

The size, in bytes, of the buffer pointed to by the <b>pData</b> member.


### -field pData

A pointer to a buffer that contains the private state data. The DXVA-HD runtime passes this buffer directly to the device without validation.


## -remarks



Use this structure for proprietary or device-specific state parameters. 

The caller allocates the <b>pData</b> array. Set the  <b>DataSize</b> member to the size of the array in bytes. When retrieving the state data, you can set <b>pData</b> to <b>NULL</b> to get the size of the data. The device will return the size in the <b>DataSize</b> member.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/cd5f56ff-61d7-49df-8114-f6a14de8e06b">DXVAHD_BLT_STATE</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/adc08662-7977-402d-9eb1-505333550fc8">IDXVAHD_VideoProcessor::SetVideoProcessBltState</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

