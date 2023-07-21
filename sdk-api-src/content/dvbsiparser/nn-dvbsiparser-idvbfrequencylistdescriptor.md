---
UID: NN:dvbsiparser.IDvbFrequencyListDescriptor
title: IDvbFrequencyListDescriptor (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDvbFrequencyListDescriptor","IDvbFrequencyListDescriptor interface [Microsoft TV Technologies]","IDvbFrequencyListDescriptor interface [Microsoft TV Technologies]","described","IDvbFrequencyListDescriptorInterface","dvbsiparser/IDvbFrequencyListDescriptor","mstv.idvbfrequencylistdescriptor"]
old-location: mstv\idvbfrequencylistdescriptor.htm
tech.root: mstv
ms.assetid: fadf7114-b9e4-4f61-816b-10725b83169a
ms.date: 12/05/2018
ms.keywords: IDvbFrequencyListDescriptor, IDvbFrequencyListDescriptor interface [Microsoft TV Technologies], IDvbFrequencyListDescriptor interface [Microsoft TV Technologies],described, IDvbFrequencyListDescriptorInterface, dvbsiparser/IDvbFrequencyListDescriptor, mstv.idvbfrequencylistdescriptor
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
 - IDvbFrequencyListDescriptor
 - dvbsiparser/IDvbFrequencyListDescriptor
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
 - IDvbFrequencyListDescriptor
---

# IDvbFrequencyListDescriptor interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbFrequencyListDescriptor</b> interface enables the client to get a frequency list descriptor from a DVB stream. The frequency list descriptor may be present in the network information table (NIT). For more information, refer to ETSI EN 300 468.

## -inheritance

The <b>IDvbFrequencyListDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbFrequencyListDescriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getnit">IDvbSiParser::GetNIT</a> to get the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_nit">IDVB_NIT</a> interface.</li>
<li>Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_nit-getrecorddescriptorbytag">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the frequency list descriptor tag (0x62). If the descriptor is present, the method returns an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>IDvbFrequencyListDescriptor</b> interface.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
