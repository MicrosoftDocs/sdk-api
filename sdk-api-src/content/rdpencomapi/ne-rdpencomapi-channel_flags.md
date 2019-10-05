---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0004
title: CHANNEL_FLAGS (rdpencomapi.h)
author: windows-sdk-content
description: Defines values for how data is sent on the channel.
old-location: rdp\channel_flags.htm
tech.root: rdp
ms.assetid: ca8a063a-81a0-44b8-8654-36a38a6f30ef
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CHANNEL_FLAGS, CHANNEL_FLAGS enumeration [RDP], CHANNEL_FLAGS_LEGACY, CHANNEL_FLAGS_UNCOMPRESSED, rdp.channel_flags, rdpencomapi/CHANNEL_FLAGS, rdpencomapi/CHANNEL_FLAGS_LEGACY, rdpencomapi/CHANNEL_FLAGS_UNCOMPRESSED
ms.topic: enum
f1_keywords: 
 - "rdpencomapi/CHANNEL_FLAGS"
dev_langs:
 - c++
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rdpencomapi.idl
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
 - Rdpencomapi.h
api_name:
 - CHANNEL_FLAGS
targetos: Windows
req.typenames: CHANNEL_FLAGS
req.redist: 
ms.custom: 19H1
---

# CHANNEL_FLAGS enumeration


## -description


Defines values for how data is sent on the channel.


## -enum-fields




### -field CHANNEL_FLAGS_LEGACY

Reserved.


### -field CHANNEL_FLAGS_UNCOMPRESSED

Data sent on the channel is not compressed. Use this option if the data is already compressed.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapivirtualchannelmanager-createvirtualchannel">IRDPSRAPIVirtualChannelManager::CreateVirtualChannel</a>
 

 

