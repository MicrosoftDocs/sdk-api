---
UID: NN:dvbsiparser.IDvbLogicalChannel2Descriptor
title: IDvbLogicalChannel2Descriptor (dvbsiparser.h)
description: Implements methods that get data from a logical channel descriptor (LCD) in a Digital Video Broadcast (DVB) MPEG-2 stream that uses the format defined in the Nordig specification used in Scandinavian countries.
helpviewer_keywords: ["IDvbLogicalChannel2Descriptor","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbLogicalChannel2Descriptor","mstv.idvblogicalchannel2descriptor"]
old-location: mstv\idvblogicalchannel2descriptor.htm
tech.root: mstv
ms.assetid: dc60db7f-ae49-48dd-bd8a-62899e5ca7a3
ms.date: 12/05/2018
ms.keywords: IDvbLogicalChannel2Descriptor, IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies], IDvbLogicalChannel2Descriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbLogicalChannel2Descriptor, mstv.idvblogicalchannel2descriptor
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbLogicalChannel2Descriptor
 - dvbsiparser/IDvbLogicalChannel2Descriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbLogicalChannel2Descriptor
---

# IDvbLogicalChannel2Descriptor interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that  get data from a logical channel descriptor (LCD) in a Digital Video Broadcast (DVB) MPEG-2 stream that uses the format defined in the Nordig specification used in Scandinavian countries.

 The logical channel descriptor may be present in the network information table (NIT).

By default, all methods in the base interface <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchanneldescriptor">IDvbLogicalChannelDescriptor</a> act on the first item in a list.  Once any  call to a <b>IDvbLogicalChannel2Descriptor</b> method completes successfully, the item that the method returns remains selected so that subsequent calls to <b>IDvbLogicalChannelDescriptor</b> methods act on the selected item.

## -inheritance

The <b>IDvbLogicalChannel2Descriptor</b> interface inherits from <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchanneldescriptor">IDvbLogicalChannelDescriptor2</a>. <b>IDvbLogicalChannel2Descriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

