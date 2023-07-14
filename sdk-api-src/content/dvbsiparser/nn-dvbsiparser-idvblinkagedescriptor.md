---
UID: NN:dvbsiparser.IDvbLinkageDescriptor
title: IDvbLinkageDescriptor (dvbsiparser.h)
description: Defines methods that get data from a Digital Video Broadcast (DVB) linkage descriptor.
helpviewer_keywords: ["IDvbLinkageDescriptor","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbLinkageDescriptor","mstv.idvblinkagedescriptor"]
old-location: mstv\idvblinkagedescriptor.htm
tech.root: mstv
ms.assetid: 4e419b50-b9c2-48e4-a484-f0fcf5c9cb7f
ms.date: 12/05/2018
ms.keywords: IDvbLinkageDescriptor, IDvbLinkageDescriptor interface [Microsoft TV Technologies], IDvbLinkageDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbLinkageDescriptor, mstv.idvblinkagedescriptor
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
 - IDvbLinkageDescriptor
 - dvbsiparser/IDvbLinkageDescriptor
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
 - IDvbLinkageDescriptor
---

# IDvbLinkageDescriptor interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Defines methods that get data from a Digital Video Broadcast (DVB) linkage descriptor. The linkage descriptor appears as part of the DVB service information in the network information table (NIT), bouquet association table (BAT), service description table (SDT), event information table (EIT), or service information table (SIT). 

The linkage descriptor identifies a service that can be presented if the consumer requests additional
information related to a service. The table that contains the linkage descriptor  indicates the entity for which additional information is available. For example, a linkage descriptor in the
NIT points to a service that provides additional information on the network, while a linkage descriptor in the BAT links to a service that provides information  about the bouquet.

## -inheritance

The <b>IDvbLinkageDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbLinkageDescriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

