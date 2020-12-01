---
UID: NF:mspaddr.CMSPAddress.PostEvent
title: CMSPAddress::PostEvent (mspaddr.h)
description: The PostEvent method is called by the MSPCall to post an event to TAPI3. This method puts the event at the end of the event list and signals TAPI3. Locks the event list.
helpviewer_keywords: ["CMSPAddress interface [TAPI 2.2]","PostEvent method","CMSPAddress.PostEvent","CMSPAddress::PostEvent","PostEvent","PostEvent method [TAPI 2.2]","PostEvent method [TAPI 2.2]","CMSPAddress interface","_tapi3_cmspaddress_postevent","mspaddr/CMSPAddress::PostEvent","tapi3.cmspaddress_postevent"]
old-location: tapi3\cmspaddress_postevent.htm
tech.root: tapi3
ms.assetid: 25050c11-c270-4fc0-85b4-0f48622a5ec5
ms.date: 12/05/2018
ms.keywords: CMSPAddress interface [TAPI 2.2],PostEvent method, CMSPAddress.PostEvent, CMSPAddress::PostEvent, PostEvent, PostEvent method [TAPI 2.2], PostEvent method [TAPI 2.2],CMSPAddress interface, _tapi3_cmspaddress_postevent, mspaddr/CMSPAddress::PostEvent, tapi3.cmspaddress_postevent
req.header: mspaddr.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPAddress::PostEvent
 - mspaddr/CMSPAddress::PostEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.PostEvent
---

# CMSPAddress::PostEvent


## -description

The 
<b>PostEvent</b> method is called by the MSPCall to post an event to TAPI3. This method puts the event at the end of the event list and signals TAPI3. Locks the event list.

## -parameters

### -param EventItem [in]

Pointer to the 
<a href="/windows/desktop/api/mspaddr/ns-mspaddr-mspeventitem">MSPEVENTITEM</a> structure, which contains the event information.

## -see-also

<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a>