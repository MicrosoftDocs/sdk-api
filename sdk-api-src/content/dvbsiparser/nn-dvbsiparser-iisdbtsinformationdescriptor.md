---
UID: NN:dvbsiparser.IIsdbTSInformationDescriptor
title: IIsdbTSInformationDescriptor (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
helpviewer_keywords: ["IIsdbTSInformationDescriptor","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","described","dvbsiparser/IIsdbTSInformationDescriptor","mstv.iisdbtsinformationdescriptor"]
old-location: mstv\iisdbtsinformationdescriptor.htm
tech.root: mstv
ms.assetid: 3c8cd33c-5c2a-48a4-9e8a-f7dd03560848
ms.date: 12/05/2018
ms.keywords: IIsdbTSInformationDescriptor, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies], IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbTSInformationDescriptor, mstv.iisdbtsinformationdescriptor
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IIsdbTSInformationDescriptor
 - dvbsiparser/IIsdbTSInformationDescriptor
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
 - IIsdbTSInformationDescriptor
---

# IIsdbTSInformationDescriptor interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor. The TS information descriptor appears in the ISDB Service Information as part of the event information table (EIT). This descriptor specifies the remote control key identifier assigned to the applicable
transport stream. It indicates the relationship between the service identifier and the transmission layer during
hierarchical transmission.

## -inheritance

The <b>IIsdbTSInformationDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IIsdbTSInformationDescriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

