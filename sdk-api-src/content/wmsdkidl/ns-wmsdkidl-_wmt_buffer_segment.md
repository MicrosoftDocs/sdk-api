---
UID: NS:wmsdkidl._WMT_BUFFER_SEGMENT
title: "_WMT_BUFFER_SEGMENT"
author: windows-sdk-content
description: The WMT_BUFFER_SEGMENT structure contains the information needed to specify a segment in a buffer. It is used as a member of the WMT_FILESINK_DATA_UNIT and WMT_PAYLOAD_FRAGMENT structures to specify segments of a packet.
old-location: wmformat\wmt_buffer_segment.htm
old-project: wmformat
ms.assetid: 047e19da-c819-46e5-8a1c-09bc93a05259
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: WMT_BUFFER_SEGMENT, WMT_BUFFER_SEGMENT structure [windows Media Format], _WMT_BUFFER_SEGMENT, wmformat.wmt_buffer_segment, wmsdkidl/WMT_BUFFER_SEGMENT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: WMT_BUFFER_SEGMENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_BUFFER_SEGMENT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _WMT_BUFFER_SEGMENT structure


## -description



The <b>WMT_BUFFER_SEGMENT</b> structure contains the information needed to specify a segment in a buffer. It is used as a member of the <a href="https://msdn.microsoft.com/e1deb01f-9f53-4ede-a3e1-13d6dc79adb5">WMT_FILESINK_DATA_UNIT</a> and <a href="https://msdn.microsoft.com/5a99c772-0e8a-4f6d-a13f-9bf7b4fa7d89">WMT_PAYLOAD_FRAGMENT</a> structures to specify segments of a packet.




## -struct-fields




### -field pBuffer

Pointer to a buffer object containing the buffer segment.


### -field cbOffset

The offset, in bytes, from the start of the buffer to the buffer segment.


### -field cbLength

The length, in bytes, of the buffer segment.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn927277">Structures</a>
 

 

