---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0005
title: "__MIDL___MIDL_itf_rdpencomapi_0000_0000_0005"
author: windows-sdk-content
description: Defines values for the type of access granted to the attendee for the channel.
old-location: rdp\channel_access_enum.htm
tech.root: Rdp
ms.assetid: 7d07954f-6514-4512-a934-6140de826ece
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CHANNEL_ACCESS_ENUM, CHANNEL_ACCESS_ENUM enumeration [RDP], CHANNEL_ACCESS_ENUM_NONE, CHANNEL_ACCESS_ENUM_SENDRECEIVE, __MIDL___MIDL_itf_rdpencomapi_0000_0000_0005, rdp.channel_access_enum, rdpencomapi/CHANNEL_ACCESS_ENUM, rdpencomapi/CHANNEL_ACCESS_ENUM_NONE, rdpencomapi/CHANNEL_ACCESS_ENUM_SENDRECEIVE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
 - CHANNEL_ACCESS_ENUM
product: Windows
targetos: Windows
req.typenames: CHANNEL_ACCESS_ENUM
req.redist: 
---

# __MIDL___MIDL_itf_rdpencomapi_0000_0000_0005 enumeration


## -description


Defines values for the type of access granted to the attendee for the channel.


## -enum-fields




### -field CHANNEL_ACCESS_ENUM_NONE

No access. The attendee cannot send or receive data on the channel.


### -field CHANNEL_ACCESS_ENUM_SENDRECEIVE

The attendee can send or receive data on the channel.


## -see-also




<a href="https://msdn.microsoft.com/7d4a19d3-b089-4689-9062-a5b52251776f">IRDPSRAPIVirtualChannel::SetAccess</a>
 

 

