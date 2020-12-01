---
UID: NS:netcon.tagNETCON_PROPERTIES
title: NETCON_PROPERTIES (netcon.h)
description: The NETCON_PROPERTIES structure stores values that describe the properties of a network connection.
helpviewer_keywords: ["NETCON_PROPERTIES","NETCON_PROPERTIES structure [ICS/ICF]","_ics_netcon_properties","ics.netcon_properties","netcon/NETCON_PROPERTIES"]
old-location: ics\netcon_properties.htm
tech.root: ics
ms.assetid: 5acda2b8-960f-41ef-9ff2-49787f4e1c0c
ms.date: 12/05/2018
ms.keywords: NETCON_PROPERTIES, NETCON_PROPERTIES structure [ICS/ICF], _ics_netcon_properties, ics.netcon_properties, netcon/NETCON_PROPERTIES
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NETCON_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagNETCON_PROPERTIES
 - netcon/tagNETCON_PROPERTIES
 - NETCON_PROPERTIES
 - netcon/NETCON_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - NetCon.h
api_name:
 - NETCON_PROPERTIES
---

# NETCON_PROPERTIES structure


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>NETCON_PROPERTIES</b> structure stores values that describe the properties of a network connection.

## -struct-fields

### -field guidId

Globally-unique identifier (GUID) for this connection.

### -field pszwName

Name of the connection itself.

### -field pszwDeviceName

Name of the device associated with the connection.

### -field Status

<a href="/windows/desktop/api/netcon/ne-netcon-netcon_status">Current status</a> of the connection.

### -field MediaType

<a href="/windows/desktop/api/netcon/ne-netcon-netcon_mediatype">Media type</a> associated with this connection.

### -field dwCharacter

<a href="/windows/desktop/api/netcon/ne-netcon-netcon_characteristic_flags">Characteristics</a> for this connection.

### -field clsidThisObject

Class identifier for the connection object.

### -field clsidUiObject

Class identifier for the user-interface object.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetconnection">INetConnection</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall
		  Reference</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-structures">Internet Connection Sharing and Internet Connection Firewall
		  Structures</a>



<a href="/windows/desktop/api/netcon/ne-netcon-netcon_characteristic_flags">NETCON_CHARACTERISTIC_FLAGS</a>



<a href="/windows/desktop/api/netcon/ne-netcon-netcon_mediatype">NETCON_MEDIATYPE</a>



<a href="/windows/desktop/api/netcon/ne-netcon-netcon_status">NETCON_STATUS</a>