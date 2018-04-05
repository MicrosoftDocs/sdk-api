---
UID: NS:bdamedia._ChannelInfo
title: "_ChannelInfo"
author: windows-driver-content
description: Contains information about the cable television channel.
old-location: mstv\channelinfo.htm
old-project: mstv
ms.assetid: 4d4c8e5b-5b9f-4cff-98c7-6d3645e677e1
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: ChannelInfo, ChannelInfo structure [Microsoft TV Technologies], _ChannelInfo, bdamedia/ChannelInfo, mstv.channelinfo
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
req.typenames: ChannelInfo
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	bdamedia.h
api_name:
-	ChannelInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _ChannelInfo structure


## -description


Contains information about the cable television channel.


## -struct-fields




### -field DVB

Contains information for DVB tuning.


### -field DVB.lONID

The original network ID.


### -field DVB.lTSID

The transport stream ID.


### -field DVB.lSID

The service ID for the network.


### -field DC

Contains information the digital cable tuning.


### -field DC.lProgNumber

The program number.


### -field ATSC

Contains information for ATSC tuning.


### -field ATSC.lProgNumber

The program number.


### -field lFrequency

The tuning frequency.

