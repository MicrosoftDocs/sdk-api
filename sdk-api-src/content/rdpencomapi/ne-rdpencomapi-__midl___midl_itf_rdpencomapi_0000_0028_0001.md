---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0028_0001
title: "__MIDL___MIDL_itf_rdpencomapi_0000_0028_0001"
author: windows-sdk-content
description: Defines values for some of the constants used in this API.
old-location: rdp\rdpencomapi_constants.htm
old-project: Rdp
ms.assetid: 50c56089-75f9-41c9-a4a4-10556f98d6e8
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: CONST_ATTENDEE_ID_DEFAULT, CONST_ATTENDEE_ID_EVERYONE, CONST_ATTENDEE_ID_HOST, CONST_CONN_INTERVAL, CONST_MAX_CHANNEL_MESSAGE_SIZE, CONST_MAX_CHANNEL_NAME_LEN, CONST_MAX_LEGACY_CHANNEL_MESSAGE_SIZE, RDPENCOMAPI_CONSTANTS, RDPENCOMAPI_CONSTANTS enumeration [RDP], __MIDL___MIDL_itf_rdpencomapi_0000_0028_0001, rdp.rdpencomapi_constants, rdpencomapi/CONST_ATTENDEE_ID_DEFAULT, rdpencomapi/CONST_ATTENDEE_ID_EVERYONE, rdpencomapi/CONST_ATTENDEE_ID_HOST, rdpencomapi/CONST_CONN_INTERVAL, rdpencomapi/CONST_MAX_CHANNEL_MESSAGE_SIZE, rdpencomapi/CONST_MAX_CHANNEL_NAME_LEN, rdpencomapi/CONST_MAX_LEGACY_CHANNEL_MESSAGE_SIZE, rdpencomapi/RDPENCOMAPI_CONSTANTS
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
req.type-library: RdpEncomAPI.tlb
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rdpencomapi.h
api_name:
-	RDPENCOMAPI_CONSTANTS
product: Windows
targetos: Windows
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_rdpencomapi_0000_0028_0001 enumeration


## -description


Defines values for some of the constants used in this API.


## -enum-fields




### -field CONST_MAX_CHANNEL_MESSAGE_SIZE

Maximum message size, in bytes.


### -field CONST_MAX_CHANNEL_NAME_LEN

Maximum length (including the null terminator) of a channel name, in characters.

Note that the legacy channel names are limited to 32 characters.


### -field CONST_MAX_LEGACY_CHANNEL_MESSAGE_SIZE

Maximum message size for a legacy channel, in bytes.

Use this constant if <b>CHANNEL_FLAGS_LEGACY</b> is set.


### -field CONST_ATTENDEE_ID_EVERYONE

Indicates all attendees.


### -field CONST_ATTENDEE_ID_HOST

Identifies the host. Used to send a virtual channel message to the host.


### -field CONST_CONN_INTERVAL

Not used.


### -field CONST_ATTENDEE_ID_DEFAULT

The default value for the <a href="https://msdn.microsoft.com/e9edd9f2-ccbf-45b2-b71c-e30368435a60">IRDPSRAPIAttendee</a>::<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a> property.

<b>Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This enumeration value is not supported before Windows 10 and Windows Server 2016.

