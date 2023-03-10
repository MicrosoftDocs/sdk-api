---
UID: NS:wmsdkidl._WMT_FILESINK_DATA_UNIT
title: WMT_FILESINK_DATA_UNIT (wmsdkidl.h)
description: The WMT_FILESINK_DATA_UNIT structure is used by IWMWriterFileSink3::OnDataUnitEx to deliver information about a packet.
helpviewer_keywords: ["WMT_FILESINK_DATA_UNIT","WMT_FILESINK_DATA_UNIT structure [windows Media Format]","wmformat.wmt_filesink_data_unit","wmsdkidl/WMT_FILESINK_DATA_UNIT"]
old-location: wmformat\wmt_filesink_data_unit.htm
tech.root: wmformat
ms.assetid: e1deb01f-9f53-4ede-a3e1-13d6dc79adb5
ms.date: 12/05/2018
ms.keywords: WMT_FILESINK_DATA_UNIT, WMT_FILESINK_DATA_UNIT structure [windows Media Format], wmformat.wmt_filesink_data_unit, wmsdkidl/WMT_FILESINK_DATA_UNIT
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: WMT_FILESINK_DATA_UNIT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMT_FILESINK_DATA_UNIT
 - wmsdkidl/_WMT_FILESINK_DATA_UNIT
 - WMT_FILESINK_DATA_UNIT
 - wmsdkidl/WMT_FILESINK_DATA_UNIT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_FILESINK_DATA_UNIT
---

# WMT_FILESINK_DATA_UNIT structure


## -description

The <b>WMT_FILESINK_DATA_UNIT</b> structure is used by <b>IWMWriterFileSink3::OnDataUnitEx</b> to deliver information about a packet.

## -struct-fields

### -field packetHeaderBuffer

A <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_buffer_segment">WMT_BUFFER_SEGMENT</a> structure specifying the buffer segment that contains the packet header.

### -field cPayloads

Count of payloads in this packet. This is also the number of elements in the array specified in <b>pPayloadHeaderBuffers</b>.

### -field pPayloadHeaderBuffers

Pointer to an array of <b>WMT_BUFFER_SEGMENT</b> structures. Each element specifies a buffer segment that contains a payload header. The number of elements is specified by <b>cPayloads</b>.

### -field cPayloadDataFragments

Count of payload data fragments in this packet. This is also the number of elements in the array pointed to by <b>pPayloadDataFragments</b>.

### -field pPayloadDataFragments

Pointer to an array of <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_payload_fragment">WMT_PAYLOAD_FRAGMENT</a> structures. Each element specifies a buffer segment that contains a payload fragment. The number of elements is specified by <b>cPayloadDataFragments</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-ondataunitex">IWMWriterFileSink3::OnDataUnitEx</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>