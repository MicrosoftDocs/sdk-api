---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0000_0004
title: "__MIDL___MIDL_itf_rdpencomapi_0000_0000_0004"
author: windows-sdk-content
description: Defines values for how data is sent on the channel.
old-location: rdp\channel_flags.htm
old-project: Rdp
ms.assetid: ca8a063a-81a0-44b8-8654-36a38a6f30ef
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: CHANNEL_FLAGS, CHANNEL_FLAGS enumeration [RDP], CHANNEL_FLAGS_LEGACY, CHANNEL_FLAGS_UNCOMPRESSED, __MIDL___MIDL_itf_rdpencomapi_0000_0000_0004, rdp.channel_flags, rdpencomapi/CHANNEL_FLAGS, rdpencomapi/CHANNEL_FLAGS_LEGACY, rdpencomapi/CHANNEL_FLAGS_UNCOMPRESSED
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rdpencomapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsTscAx.dll
tech.root: 
req.typenames: CHANNEL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rdpencomapi.h
api_name:
 - CHANNEL_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
req.product: ADAM
---

# __MIDL___MIDL_itf_rdpencomapi_0000_0000_0004 enumeration


## -description


Defines values for how data is sent on the channel.


## -enum-fields




### -field CHANNEL_FLAGS_LEGACY

Reserved.


### -field CHANNEL_FLAGS_UNCOMPRESSED

Data sent on the channel is not compressed. Use this option if the data is already compressed.


## -see-also




<a href="https://msdn.microsoft.com/0185af26-a29d-4227-bad6-2633de18617e">IRDPSRAPIVirtualChannelManager::CreateVirtualChannel</a>
 

 

