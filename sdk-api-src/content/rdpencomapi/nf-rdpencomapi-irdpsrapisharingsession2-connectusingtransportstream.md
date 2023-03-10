---
UID: NF:rdpencomapi.IRDPSRAPISharingSession2.ConnectUsingTransportStream
title: IRDPSRAPISharingSession2::ConnectUsingTransportStream (rdpencomapi.h)
description: Connects using the specified transport stream.
helpviewer_keywords: ["ConnectUsingTransportStream","ConnectUsingTransportStream method [RDP]","ConnectUsingTransportStream method [RDP]","IRDPSRAPISharingSession2 interface","IRDPSRAPISharingSession2 interface [RDP]","ConnectUsingTransportStream method","IRDPSRAPISharingSession2.ConnectUsingTransportStream","IRDPSRAPISharingSession2::ConnectUsingTransportStream","rdp.irdpsrapisharingsession2_connectusingtransportstream","rdpencomapi/IRDPSRAPISharingSession2::ConnectUsingTransportStream"]
old-location: rdp\irdpsrapisharingsession2_connectusingtransportstream.htm
tech.root: rdp
ms.assetid: 78f517c9-0870-4dfd-a318-3bd510e05dfa
ms.date: 12/05/2018
ms.keywords: ConnectUsingTransportStream, ConnectUsingTransportStream method [RDP], ConnectUsingTransportStream method [RDP],IRDPSRAPISharingSession2 interface, IRDPSRAPISharingSession2 interface [RDP],ConnectUsingTransportStream method, IRDPSRAPISharingSession2.ConnectUsingTransportStream, IRDPSRAPISharingSession2::ConnectUsingTransportStream, rdp.irdpsrapisharingsession2_connectusingtransportstream, rdpencomapi/IRDPSRAPISharingSession2::ConnectUsingTransportStream
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPISharingSession2::ConnectUsingTransportStream
 - rdpencomapi/IRDPSRAPISharingSession2::ConnectUsingTransportStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPISharingSession2.ConnectUsingTransportStream
---

# IRDPSRAPISharingSession2::ConnectUsingTransportStream


## -description

Connects using the specified transport stream.

## -parameters

### -param pStream [in]

The transport stream used for the connection.

### -param bstrGroup [in]

The name of the group. The string must be unique for the session. Applications typically use the group name to separate attendees into groups that can be granted different authorization levels.

### -param bstrAuthenticatedAttendeeName [in]

The name of the authenticated attendee.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>