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

# IWMStreamConfig::SetBitrate


## -description



The <b>SetBitrate</b> method specifies the bit rate for the stream.




## -parameters




### -param pdwBitrate






#### - dwBitrate [in]

<b>DWORD</b> containing the bit rate, in bits per second.


## -returns



This method always returns S_OK.




## -remarks



The bit rate is the number of bits per second given to the stream in the ASF file, not including any overhead. For compressed bit streams, such as audio or video, a higher bit rate gives higher quality.

The new value will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/e013996a-95b6-4cd3-9fb5-75dbce821eef">IWMStreamConfig Interface</a>



<a href="https://msdn.microsoft.com/d34bea45-758e-4c4a-928f-229ce6b4241c">IWMStreamConfig::GetBitrate</a>
 

 

