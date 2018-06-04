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

# _MFNETSOURCE_PROTOCOL_TYPE enumeration


## -description



          Indicates the type of control protocol that is used in streaming or downloading.
        


## -enum-fields




### -field MFNETSOURCE_UNDEFINED


            The protocol type has not yet been determined.
          


### -field MFNETSOURCE_HTTP


            The protocol type is HTTP. This includes HTTPv9, WMSP, and HTTP download.
          


### -field MFNETSOURCE_RTSP


            The protocol type is Real Time Streaming Protocol (RTSP).
          


### -field MFNETSOURCE_FILE


            The content is read from a file. The file might be local or on a remote share.
          


### -field MFNETSOURCE_MULTICAST

The protocol type is multicast.

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/51cd90cf-a3ae-45dd-bc27-c91d44cab9f5">IMFNetSchemeHandlerConfig::GetSupportedProtocolType</a>



<a href="https://msdn.microsoft.com/4956e003-7f52-40af-8f6b-b1b73ba2a897">MFNETSOURCE_STATISTICS_IDS</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/3c026426-c2b7-4909-9524-9cc0bd45347e">Supported Protocols</a>
 

 

