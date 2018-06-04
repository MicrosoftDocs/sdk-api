---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

