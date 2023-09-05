---
UID: NN:dvbsiparser.IDvbLogicalChannelDescriptor
title: IDvbLogicalChannelDescriptor (dvbsiparser.h)
description: The IDvbLogicalChannelDescriptor interface enables the client to get a logical channel descriptor from a DVB stream.
helpviewer_keywords: ["IDvbLogicalChannelDescriptor","IDvbLogicalChannelDescriptor interface [DirectShow]","IDvbLogicalChannelDescriptor interface [DirectShow]","described","IDvbLogicalChannelDescriptorInterface","dvbsiparser/IDvbLogicalChannelDescriptor","mstv.idvblogicalchanneldescriptor"]
old-location: mstv\idvblogicalchanneldescriptor.htm
tech.root: mstv
ms.assetid: 6e0a99e9-088f-420c-bb60-2d324aa28227
ms.date: 12/05/2018
ms.keywords: IDvbLogicalChannelDescriptor, IDvbLogicalChannelDescriptor interface [DirectShow], IDvbLogicalChannelDescriptor interface [DirectShow],described, IDvbLogicalChannelDescriptorInterface, dvbsiparser/IDvbLogicalChannelDescriptor, mstv.idvblogicalchanneldescriptor
req.header: dvbsiparser.h
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
 - IDvbLogicalChannelDescriptor
 - dvbsiparser/IDvbLogicalChannelDescriptor
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
 - IDvbLogicalChannelDescriptor
---

# IDvbLogicalChannelDescriptor interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        </div>
<div> </div>


The <b>IDvbLogicalChannelDescriptor</b> interface enables the client to get a logical channel descriptor from a DVB stream. The logical channel descriptor may be present in the network information table (NIT).

## -inheritance

The <b>IDvbLogicalChannelDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbLogicalChannelDescriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getnit">IDvbSiParser::GetNIT</a> to get the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_nit">IDVB_NIT</a> interface.</li>
<li>Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_nit-getrecorddescriptorbytag">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the logical channel descriptor tag (0x83). If the descriptor is present, the method returns an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> pointer for the <b>IDvbLogicalChannelDescriptor</b> interface.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
