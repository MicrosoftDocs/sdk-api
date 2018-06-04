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

# IRawCDImageTrackInfo::get_DigitalAudioCopySetting


## -description


Retrieves the value for the bit that represents the current digital audio copy setting on the resulting media.  Please see the <a href="https://msdn.microsoft.com/6bc38584-2e44-4c1a-b5bb-a91c0ffe7e6b">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a> enumeration for possible values.




## -parameters




### -param value [out]

The current digital audio copy setting.


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation.




## -remarks



This property may only be set for tracks containing audio data.

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the <a href="http://go.microsoft.com/fwlink/p/?linkid=141659">Windows Feature Pack for Storage</a>. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.




## -see-also




<a href="https://msdn.microsoft.com/6bc38584-2e44-4c1a-b5bb-a91c0ffe7e6b">IMAPI_CD_TRACK_DIGITAL_COPY_SETTING</a>



<a href="https://msdn.microsoft.com/5d074279-35fb-48d0-b298-c1a83f57d805">IRawCDImageTrackInfo</a>
 

 

