---
UID: NE:mfidl._MFNETSOURCE_PROTOCOL_TYPE
title: "_MFNETSOURCE_PROTOCOL_TYPE"
author: windows-sdk-content
description: Indicates the type of control protocol that is used in streaming or downloading.
old-location: mf\mfnetsource_protocol_type.htm
old-project: medfound
ms.assetid: dd628b9e-3c52-4c14-aa0f-5e0b811d3f57
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: MFNETSOURCE_FILE, MFNETSOURCE_HTTP, MFNETSOURCE_MULTICAST, MFNETSOURCE_PROTOCOL_TYPE, MFNETSOURCE_PROTOCOL_TYPE enumeration [Media Foundation], MFNETSOURCE_RTSP, MFNETSOURCE_UNDEFINED, _MFNETSOURCE_PROTOCOL_TYPE, dd628b9e-3c52-4c14-aa0f-5e0b811d3f57, mf.mfnetsource_protocol_type, mfidl/MFNETSOURCE_FILE, mfidl/MFNETSOURCE_HTTP, mfidl/MFNETSOURCE_MULTICAST, mfidl/MFNETSOURCE_PROTOCOL_TYPE, mfidl/MFNETSOURCE_RTSP, mfidl/MFNETSOURCE_UNDEFINED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: MFNETSOURCE_PROTOCOL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfidl.h
api_name:
 - MFNETSOURCE_PROTOCOL_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

