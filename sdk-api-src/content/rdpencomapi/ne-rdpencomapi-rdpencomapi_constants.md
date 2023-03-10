---
UID: NE:rdpencomapi.__MIDL___MIDL_itf_rdpencomapi_0000_0028_0001
title: RDPENCOMAPI_CONSTANTS (rdpencomapi.h)
description: Defines values for some of the constants used in this API.
helpviewer_keywords: ["CONST_ATTENDEE_ID_DEFAULT","CONST_ATTENDEE_ID_EVERYONE","CONST_ATTENDEE_ID_HOST","CONST_CONN_INTERVAL","CONST_MAX_CHANNEL_MESSAGE_SIZE","CONST_MAX_CHANNEL_NAME_LEN","CONST_MAX_LEGACY_CHANNEL_MESSAGE_SIZE","RDPENCOMAPI_CONSTANTS","RDPENCOMAPI_CONSTANTS enumeration [RDP]","rdp.rdpencomapi_constants","rdpencomapi/CONST_ATTENDEE_ID_DEFAULT","rdpencomapi/CONST_ATTENDEE_ID_EVERYONE","rdpencomapi/CONST_ATTENDEE_ID_HOST","rdpencomapi/CONST_CONN_INTERVAL","rdpencomapi/CONST_MAX_CHANNEL_MESSAGE_SIZE","rdpencomapi/CONST_MAX_CHANNEL_NAME_LEN","rdpencomapi/CONST_MAX_LEGACY_CHANNEL_MESSAGE_SIZE","rdpencomapi/RDPENCOMAPI_CONSTANTS"]
old-location: rdp\rdpencomapi_constants.htm
tech.root: rdp
ms.assetid: 50c56089-75f9-41c9-a4a4-10556f98d6e8
ms.date: 12/05/2018
ms.keywords: CONST_ATTENDEE_ID_DEFAULT, CONST_ATTENDEE_ID_EVERYONE, CONST_ATTENDEE_ID_HOST, CONST_CONN_INTERVAL, CONST_MAX_CHANNEL_MESSAGE_SIZE, CONST_MAX_CHANNEL_NAME_LEN, CONST_MAX_LEGACY_CHANNEL_MESSAGE_SIZE, RDPENCOMAPI_CONSTANTS, RDPENCOMAPI_CONSTANTS enumeration [RDP], rdp.rdpencomapi_constants, rdpencomapi/CONST_ATTENDEE_ID_DEFAULT, rdpencomapi/CONST_ATTENDEE_ID_EVERYONE, rdpencomapi/CONST_ATTENDEE_ID_HOST, rdpencomapi/CONST_CONN_INTERVAL, rdpencomapi/CONST_MAX_CHANNEL_MESSAGE_SIZE, rdpencomapi/CONST_MAX_CHANNEL_NAME_LEN, rdpencomapi/CONST_MAX_LEGACY_CHANNEL_MESSAGE_SIZE, rdpencomapi/RDPENCOMAPI_CONSTANTS
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
req.typenames: RDPENCOMAPI_CONSTANTS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_rdpencomapi_0000_0028_0001
 - rdpencomapi/__MIDL___MIDL_itf_rdpencomapi_0000_0028_0001
 - RDPENCOMAPI_CONSTANTS
 - rdpencomapi/RDPENCOMAPI_CONSTANTS
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
 - RDPENCOMAPI_CONSTANTS
---

# RDPENCOMAPI_CONSTANTS enumeration


## -description

Defines values for some of the constants used in this API.

## -enum-fields

### -field CONST_MAX_CHANNEL_MESSAGE_SIZE:1024

Maximum message size, in bytes.

### -field CONST_MAX_CHANNEL_NAME_LEN:8

Maximum length (including the null terminator) of a channel name, in characters.

Note that the legacy channel names are limited to 32 characters.

### -field CONST_MAX_LEGACY_CHANNEL_MESSAGE_SIZE:409600

Maximum message size for a legacy channel, in bytes.

Use this constant if <b>CHANNEL_FLAGS_LEGACY</b> is set.

### -field CONST_ATTENDEE_ID_EVERYONE:-1

Indicates all attendees.

### -field CONST_ATTENDEE_ID_HOST:0

Identifies the host. Used to send a virtual channel message to the host.

### -field CONST_CONN_INTERVAL:50

Not used.

### -field CONST_ATTENDEE_ID_DEFAULT:0xffffffff

The default value for the <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiattendee">IRDPSRAPIAttendee</a>::<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiattendee-get_id">Id</a> property.

<b>Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:  </b>This enumeration value is not supported before Windows 10 and Windows Server 2016.
