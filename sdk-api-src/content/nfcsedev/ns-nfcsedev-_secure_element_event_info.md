---
UID: NS:nfcsedev._SECURE_ELEMENT_EVENT_INFO
title: "_SECURE_ELEMENT_EVENT_INFO"
author: windows-driver-content
description: This structure provides information about a secure element event.
old-location: nfpdrivers\secure_element_event_info.htm
old-project: nfpdrivers
ms.assetid: 72B31C26-89D3-49B2-A404-E6F096D0A334
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: "*PSECURE_ELEMENT_EVENT_INFO, PSECURE_ELEMENT_EVENT_INFO, PSECURE_ELEMENT_EVENT_INFO structure pointer [Near-Field Proximity Drivers], SECURE_ELEMENT_EVENT_INFO, SECURE_ELEMENT_EVENT_INFO structure [Near-Field Proximity Drivers], _SECURE_ELEMENT_EVENT_INFO, nfcsedev/PSECURE_ELEMENT_EVENT_INFO, nfcsedev/SECURE_ELEMENT_EVENT_INFO, nfpdrivers.secure_element_event_info"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: nfcsedev.h
req.include-header: 
req.target-type: Windows
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
req.typenames: SECURE_ELEMENT_EVENT_INFO, *PSECURE_ELEMENT_EVENT_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	nfcsedev.h
api_name:
-	SECURE_ELEMENT_EVENT_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# _SECURE_ELEMENT_EVENT_INFO structure


## -description


This structure provides information about a secure element event.


## -struct-fields




### -field guidSecureElementId

This is a unique identifier for the secure element.


### -field eEventType

This is an event type. For more information about the types, see the <a href="https://msdn.microsoft.com/library/windows/hardware/dn905623">SECURE_ELEMENT_EVENT_TYPE</a> enumeration topic.


### -field cbEventData

This is the amount of bytes for the pbEventData array.


### -field pbEventData

 




#### - pbEventData[ANYSIZE_ARRAY]

This is the event data buffer. When <b>eEventType</b> is <b>HceActivated</b> or <b>HceDeactivated</b>, this member contains a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn905592">SECURE_ELEMENT_HCE_ACTIVATION_PAYLOAD</a> structure. The <b>bConnectionId</b> member in that structure is the same ID value that’s used in <a href="https://msdn.microsoft.com/library/windows/hardware/dn905624">SECURE_ELEMENT_HCE_DATA_PACKET</a> to send and receive an HCE packet with <a href="https://msdn.microsoft.com/library/windows/hardware/dn905511">IOCTL_NFCSE_HCE_REMOTE_SEND</a> and <a href="https://msdn.microsoft.com/library/windows/hardware/dn905510">IOCTL_NFCSE_HCE_REMOTE_RECV</a>.

When <b>eEventType</b> is <b>ExternalReaderArrival</b> or <b>ExternalReaderDeparture</b>, <b>pbEventData</b> is empty and <b>cbEventData</b> is 0.

When <b>eEventType</b> is <b>Transaction</b>, <b>pbEventData</b> contains a list of parameters that is encoded in BER-TLV fields. This event is mapped to EVT_TRANSACTION.

