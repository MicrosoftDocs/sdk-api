---
UID: NS:eapmethodtypes.tagEapPacket
title: EapPacket (eapmethodtypes.h)
description: Contains a packet of opaque data sent during an EAP authentication session.
helpviewer_keywords: ["EapPacket","EapPacket structure [EAPHost]","eaphost.eappacket","eapmethodtypes/EapPacket"]
old-location: eaphost\eappacket.htm
tech.root: eaphost
ms.assetid: a5d78db0-990f-4318-8f1a-4e903221845f
ms.date: 12/05/2018
ms.keywords: EapPacket, EapPacket structure [EAPHost], eaphost.eappacket, eapmethodtypes/EapPacket
req.header: eapmethodtypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: EapPacket
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagEapPacket
 - eapmethodtypes/tagEapPacket
 - EapPacket
 - eapmethodtypes/EapPacket
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - eapmethodtypes.h
api_name:
 - EapPacket
---

# EapPacket structure


## -description

 The <b>EapPacket</b> structure contains a packet of opaque data sent during an EAP authentication session.

## -struct-fields

### -field Code

An <a href="/windows/desktop/api/eapmethodtypes/ne-eapmethodtypes-eapcode">EapCode</a> enumeration value that identifies the packet type.

### -field Id

The packet ID number.

### -field Length

The length of the entire packet

### -field Data

The packet message data. This opaque data block continues after the first byte for <b>Length</b> - 1 bytes.

## -see-also

[Common EAPHost API Structures](/windows/win32/eaphost/common-eap-host-api-structures)



<a href="/windows/desktop/api/eapmethodtypes/ne-eapmethodtypes-eapcode">EapCode</a>