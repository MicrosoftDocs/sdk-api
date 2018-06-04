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

# _WMT_WEBSTREAM_FORMAT structure


## -description



The <b>WMT_WEBSTREAM_FORMAT</b> structure contains information about a Web stream. This structure is used as the <b>pbFormat</b> member of the <a href="https://msdn.microsoft.com/37a9ac59-e152-47e1-96ee-b816cd645936">WM_MEDIA_TYPE</a> structure for Web streams.




## -struct-fields




### -field cbSize

<b>WORD</b> containing the size of the structure, in bytes.


### -field cbSampleHeaderFixedData

<b>WORD</b> containing the size of Web stream sample header, in bytes.


### -field wVersion

<b>WORD</b> containing the version number. Set to 1 for streams created with the Windows Media Format 9 Series SDK.


### -field wReserved

<b>WORD</b>. Reserved.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

