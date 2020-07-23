---
UID: NE:mfidl._MFNETSOURCE_PROTOCOL_TYPE
title: MFNETSOURCE_PROTOCOL_TYPE (mfidl.h)
description: Indicates the type of control protocol that is used in streaming or downloading.
helpviewer_keywords: ["MFNETSOURCE_FILE","MFNETSOURCE_HTTP","MFNETSOURCE_MULTICAST","MFNETSOURCE_PROTOCOL_TYPE","MFNETSOURCE_PROTOCOL_TYPE enumeration [Media Foundation]","MFNETSOURCE_RTSP","MFNETSOURCE_UNDEFINED","dd628b9e-3c52-4c14-aa0f-5e0b811d3f57","mf.mfnetsource_protocol_type","mfidl/MFNETSOURCE_FILE","mfidl/MFNETSOURCE_HTTP","mfidl/MFNETSOURCE_MULTICAST","mfidl/MFNETSOURCE_PROTOCOL_TYPE","mfidl/MFNETSOURCE_RTSP","mfidl/MFNETSOURCE_UNDEFINED"]
old-location: mf\mfnetsource_protocol_type.htm
tech.root: mf
ms.assetid: dd628b9e-3c52-4c14-aa0f-5e0b811d3f57
ms.date: 12/05/2018
ms.keywords: MFNETSOURCE_FILE, MFNETSOURCE_HTTP, MFNETSOURCE_MULTICAST, MFNETSOURCE_PROTOCOL_TYPE, MFNETSOURCE_PROTOCOL_TYPE enumeration [Media Foundation], MFNETSOURCE_RTSP, MFNETSOURCE_UNDEFINED, dd628b9e-3c52-4c14-aa0f-5e0b811d3f57, mf.mfnetsource_protocol_type, mfidl/MFNETSOURCE_FILE, mfidl/MFNETSOURCE_HTTP, mfidl/MFNETSOURCE_MULTICAST, mfidl/MFNETSOURCE_PROTOCOL_TYPE, mfidl/MFNETSOURCE_RTSP, mfidl/MFNETSOURCE_UNDEFINED
f1_keywords:
- mfidl/MFNETSOURCE_PROTOCOL_TYPE
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- mfidl.h
api_name:
- MFNETSOURCE_PROTOCOL_TYPE
targetos: Windows
req.typenames: MFNETSOURCE_PROTOCOL_TYPE
req.redist: 
ms.custom: 19H1
---

# MFNETSOURCE_PROTOCOL_TYPE enumeration


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




<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfnetschemehandlerconfig-getsupportedprotocoltype">IMFNetSchemeHandlerConfig::GetSupportedProtocolType</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids">MFNETSOURCE_STATISTICS_IDS</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/supported-protocols">Supported Protocols</a>
 

 

