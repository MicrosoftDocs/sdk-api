---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0005
title: CHANNEL_ACCESS_ENUM (rdpencomapi.h)
description: Defines values for the type of access granted to the attendee for the channel.
helpviewer_keywords: ["CHANNEL_ACCESS_ENUM","CHANNEL_ACCESS_ENUM enumeration [RDP]","CHANNEL_ACCESS_ENUM_NONE","CHANNEL_ACCESS_ENUM_SENDRECEIVE","rdp.channel_access_enum","rdpencomapi/CHANNEL_ACCESS_ENUM","rdpencomapi/CHANNEL_ACCESS_ENUM_NONE","rdpencomapi/CHANNEL_ACCESS_ENUM_SENDRECEIVE"]
old-location: rdp\channel_access_enum.htm
tech.root: rdp
ms.assetid: 7d07954f-6514-4512-a934-6140de826ece
ms.date: 12/05/2018
ms.keywords: CHANNEL_ACCESS_ENUM, CHANNEL_ACCESS_ENUM enumeration [RDP], CHANNEL_ACCESS_ENUM_NONE, CHANNEL_ACCESS_ENUM_SENDRECEIVE, rdp.channel_access_enum, rdpencomapi/CHANNEL_ACCESS_ENUM, rdpencomapi/CHANNEL_ACCESS_ENUM_NONE, rdpencomapi/CHANNEL_ACCESS_ENUM_SENDRECEIVE
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
req.typenames: CHANNEL_ACCESS_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_rdpencomapi_0000_0000_0005
 - rdpencomapi/__MIDL___MIDL_itf_rdpencomapi_0000_0000_0005
 - CHANNEL_ACCESS_ENUM
 - rdpencomapi/CHANNEL_ACCESS_ENUM
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
 - CHANNEL_ACCESS_ENUM
---

# CHANNEL_ACCESS_ENUM enumeration


## -description

Defines values for the type of access granted to the attendee for the channel.

## -enum-fields

### -field CHANNEL_ACCESS_ENUM_NONE:0

No access. The attendee cannot send or receive data on the channel.

### -field CHANNEL_ACCESS_ENUM_SENDRECEIVE

The attendee can send or receive data on the channel.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapivirtualchannel-setaccess">IRDPSRAPIVirtualChannel::SetAccess</a>
