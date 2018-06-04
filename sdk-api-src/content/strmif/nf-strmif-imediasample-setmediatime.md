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

# IMediaSample::SetMediaTime


## -description



The <code>SetMediaTime</code> method sets the media times for this sample.




## -parameters




### -param pTimeStart [in]

Pointer to the beginning media time.


### -param pTimeEnd [in]

Pointer to the ending media time.


## -returns



Returns S_OK, or an <b>HRESULT</b> value indicating the cause of the error.




## -remarks



To invalidate the media time, set <i>pTimeStart</i> and <i>pTimeEnd</i> to <b>NULL</b>. This will cause the <a href="https://msdn.microsoft.com/eb2a8fd4-4a25-482c-8509-f43461c708d6">IMediaSample::GetMediaTime</a> method to return VFW_E_MEDIA_TIME_NOT_SET.

For more information about media times, see <a href="https://msdn.microsoft.com/445fe6b9-9d5b-45fd-9c9e-8c632c5228ae">Time Stamps</a>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/883e5e3b-db91-4806-96cc-c6f8cddfcca6">IMediaSample Interface</a>
 

 

