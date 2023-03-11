---
UID: NS:icodecapi.CodecAPIEventData
title: CodecAPIEventData
ms.date: 08/05/2022
targetos: Windows
description: The CodecAPIEventData structure contains event data for the EC_CODECAPI_EVENT event and is sent by codecs that support the ICodecAPI interface.
helpviewer_keywords: ["CodecAPIEventData","CodecAPIEventData structure [DirectShow]","CodecAPIEventDataStructure","dshow.codecapieventdata","icodecapi/CodecAPIEventData"]
tech.root: mf
req.construct-type: structure
req.ddi-compliance: 
req.dll: 
req.header: icodecapi.h
req.include-header: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.typenames: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - icodecapi.h
api_name:
 - CodecAPIEventData
f1_keywords:
 - CodecAPIEventData
 - icodecapi/CodecAPIEventData
dev_langs:
 - c++
---

## -description

The <b>CodecAPIEventData</b> structure contains event data for the <a href="/windows/desktop/DirectShow/ec-codecapi-event">EC_CODECAPI_EVENT</a> event. This event is sent by codecs that support the <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi">ICodecAPI</a> interface.

## -struct-fields

### -field guid

A GUID that identifies the codec event.

### -field dataLength

The length of the additional data that follows this structure, in bytes.
          The value can be zero.

### -field reserved

Reserved; do not use.

## -remarks


This structure may be followed by addition data, depending on the codec event. For more information, see <a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-registerforevent">ICodecAPI::RegisterForEvent</a>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/api/icodecapi/nf-icodecapi-icodecapi-registerforevent">ICodecAPI::RegisterForEvent</a>
