---
UID: NS:strmif.CodecAPIEventData
title: CodecAPIEventData
author: windows-sdk-content
description: The CodecAPIEventData structure contains event data for the EC_CODECAPI_EVENT event. This event is sent by codecs that support the ICodecAPI interface.
old-location: dshow\codecapieventdata.htm
old-project: DirectShow
ms.assetid: 04d0177d-ec9d-4f23-abd1-a37c787c24b2
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: CodecAPIEventData, CodecAPIEventData structure [DirectShow], CodecAPIEventDataStructure, dshow.codecapieventdata, strmif/CodecAPIEventData
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - CodecAPIEventData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# CodecAPIEventData structure


## -description



The <b>CodecAPIEventData</b> structure contains event data for the <a href="https://msdn.microsoft.com/88924ba9-707b-41a7-9bca-c630b4a9c4c8">EC_CODECAPI_EVENT</a> event. This event is sent by codecs that support the <a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI</a> interface.




## -struct-fields




### -field guid


            A GUID that identifies the codec event.
          


### -field dataLength


            The length of the additional data that follows this structure, in bytes.
          The value can be zero.


### -field reserved


            Reserved; do not use.
          


## -remarks



This structure may be followed by addition data, depending on the codec event. For more information, see <a href="https://msdn.microsoft.com/87423ddb-7011-40ab-a449-eb43688efb26">ICodecAPI::RegisterForEvent</a>
    .




## -see-also




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/87423ddb-7011-40ab-a449-eb43688efb26">ICodecAPI::RegisterForEvent</a>
 

 

