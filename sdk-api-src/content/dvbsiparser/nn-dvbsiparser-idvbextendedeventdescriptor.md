---
UID: NN:dvbsiparser.IDvbExtendedEventDescriptor
title: IDvbExtendedEventDescriptor (dvbsiparser.h)
description: Implements methods that get data from a Digital Video Broadcast (DVB) extended event descriptor.
helpviewer_keywords: ["IDvbExtendedEventDescriptor","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IDvbExtendedEventDescriptor","mstv.idvbextendedeventdescriptor"]
old-location: mstv\idvbextendedeventdescriptor.htm
tech.root: mstv
ms.assetid: db100f17-f7b8-4252-8090-44567ab9dcbe
ms.date: 12/05/2018
ms.keywords: IDvbExtendedEventDescriptor, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies], IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbExtendedEventDescriptor, mstv.idvbextendedeventdescriptor
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
 - IDvbExtendedEventDescriptor
 - dvbsiparser/IDvbExtendedEventDescriptor
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
 - IDvbExtendedEventDescriptor
---

# IDvbExtendedEventDescriptor interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that get data  from a Digital Video Broadcast (DVB) extended event descriptor. An extended  event descriptor appears as part of the DVB service information in the event information table (EIT) and service information table (SIT). The descriptor provides a detailed text description of an event that may be used in addition to the
short event descriptor. More than one extended event descriptor can be associated to allow more than 256 bytes of information about one event
to be conveyed. Text information can be structured into two columns, one that provides an
item description field, and one that provides the item text, for example, to include a cast list in a movie or show description.

## -inheritance

The <b>IDvbExtendedEventDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbExtendedEventDescriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

