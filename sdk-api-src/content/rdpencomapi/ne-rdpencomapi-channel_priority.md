---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0003
title: CHANNEL_PRIORITY (rdpencomapi.h)
description: Defines values for the priority used to send packets on the channel.
helpviewer_keywords: ["CHANNEL_PRIORITY","CHANNEL_PRIORITY enumeration [RDP]","CHANNEL_PRIORITY_HI","CHANNEL_PRIORITY_LO","CHANNEL_PRIORITY_MED","rdp.channel_priority","rdpencomapi/CHANNEL_PRIORITY","rdpencomapi/CHANNEL_PRIORITY_HI","rdpencomapi/CHANNEL_PRIORITY_LO","rdpencomapi/CHANNEL_PRIORITY_MED"]
old-location: rdp\channel_priority.htm
tech.root: rdp
ms.assetid: 8b472714-dcd2-4da9-83cf-64e846417456
ms.date: 12/05/2018
ms.keywords: CHANNEL_PRIORITY, CHANNEL_PRIORITY enumeration [RDP], CHANNEL_PRIORITY_HI, CHANNEL_PRIORITY_LO, CHANNEL_PRIORITY_MED, rdp.channel_priority, rdpencomapi/CHANNEL_PRIORITY, rdpencomapi/CHANNEL_PRIORITY_HI, rdpencomapi/CHANNEL_PRIORITY_LO, rdpencomapi/CHANNEL_PRIORITY_MED
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
targetos: Windows
req.typenames: CHANNEL_PRIORITY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_rdpencomapi_0000_0000_0003
 - rdpencomapi/__MIDL___MIDL_itf_rdpencomapi_0000_0000_0003
 - CHANNEL_PRIORITY
 - rdpencomapi/CHANNEL_PRIORITY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rdpencomapi.h
api_name:
 - CHANNEL_PRIORITY
---

# CHANNEL_PRIORITY enumeration


## -description

Defines values for the priority used to send packets on the channel.

## -enum-fields

### -field CHANNEL_PRIORITY_LO:0

Send the packets at a low priority.

### -field CHANNEL_PRIORITY_MED

Send the packets at a medium priority.

### -field CHANNEL_PRIORITY_HI

Send the packets at a high priority.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapivirtualchannel-get_priority">Priority Property of IRDPSRAPIVirtualChannel</a>
