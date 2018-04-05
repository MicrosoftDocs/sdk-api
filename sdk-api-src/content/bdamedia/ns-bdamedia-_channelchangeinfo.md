---
UID: NS:bdamedia._ChannelChangeInfo
title: "_ChannelChangeInfo"
author: windows-driver-content
description: Contains information about a channel-change event in an MPEG-2 stream.
old-location: mstv\channelchangeinfo.htm
old-project: mstv
ms.assetid: 61130e8e-7000-4f5a-b4c1-7ae22cfad473
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ChannelChangeInfo, ChannelChangeInfo structure [Microsoft TV Technologies], _ChannelChangeInfo, bdamedia/ChannelChangeInfo, mstv.channelchangeinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: bdamedia.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: ChannelChangeInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdamedia.h
api_name:
-	ChannelChangeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _ChannelChangeInfo structure


## -description


Contains information about a channel-change event in an MPEG-2 stream.


## -struct-fields




### -field state

Specifies the  event state, specified as a member of the <a href="https://msdn.microsoft.com/21ed5fdf-1e48-4020-8bff-6f7f9ed0ac12">ChannelChangeSpanningEvent_State</a> enumeration.


### -field TimeStamp

The tick count from the system timer when the event occurred.

