---
UID: NS:wmsdkidl._WMT_PAYLOAD_FRAGMENT
title: "_WMT_PAYLOAD_FRAGMENT"
author: windows-sdk-content
description: The WMT_PAYLOAD_FRAGMENT structure contains the information needed to extract a payload fragment from a buffer and identifies the payload to which the fragment belongs.
old-location: wmformat\wmt_payload_fragment.htm
tech.root: wmformat
ms.assetid: 5a99c772-0e8a-4f6d-a13f-9bf7b4fa7d89
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: WMT_PAYLOAD_FRAGMENT, WMT_PAYLOAD_FRAGMENT structure [windows Media Format], _WMT_PAYLOAD_FRAGMENT, wmformat.wmt_payload_fragment, wmsdkidl/WMT_PAYLOAD_FRAGMENT
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WMT_PAYLOAD_FRAGMENT
product: Windows
targetos: Windows
req.typenames: WMT_PAYLOAD_FRAGMENT
req.redist: 
---

# _WMT_PAYLOAD_FRAGMENT structure


## -description



The <b>WMT_PAYLOAD_FRAGMENT</b> structure contains the information needed to extract a payload fragment from a buffer and identifies the payload to which the fragment belongs. An array of <b>WMT_PAYLOAD_FRAGMENT</b> structures is used as a member of the <b>WMT_FILESINK_DATA_UNIT</b> structure to provide access to each payload fragment in a packet.




## -struct-fields




### -field dwPayloadIndex

<b>DWORD</b> containing the payload index. This identifies the payload item to which this fragment belongs.


### -field segmentData

A <b>WMT_BUFFER_SEGMENT</b> structure specifying the buffer segment containing the payload fragment.


## -see-also




<a href="https://msdn.microsoft.com/118ef278-ca4f-4c30-9633-a2d851f5c758">Structures</a>
 

 

