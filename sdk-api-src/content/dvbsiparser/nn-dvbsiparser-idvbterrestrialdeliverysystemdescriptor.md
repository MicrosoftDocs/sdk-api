---
UID: NN:dvbsiparser.IDvbTerrestrialDeliverySystemDescriptor
title: IDvbTerrestrialDeliverySystemDescriptor (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDvbTerrestrialDeliverySystemDescriptor","IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies]","IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies]","described","IDvbTerrestrialDeliverySystemDescriptorInterface","dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor","mstv.idvbterrestrialdeliverysystemdescriptor"]
old-location: mstv\idvbterrestrialdeliverysystemdescriptor.htm
tech.root: mstv
ms.assetid: 7000f937-2f58-43c1-b0e1-60d3171485b0
ms.date: 12/05/2018
ms.keywords: IDvbTerrestrialDeliverySystemDescriptor, IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies], IDvbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],described, IDvbTerrestrialDeliverySystemDescriptorInterface, dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor, mstv.idvbterrestrialdeliverysystemdescriptor
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
 - IDvbTerrestrialDeliverySystemDescriptor
 - dvbsiparser/IDvbTerrestrialDeliverySystemDescriptor
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
 - IDvbTerrestrialDeliverySystemDescriptor
---

# IDvbTerrestrialDeliverySystemDescriptor interface


## -description

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDvbTerrestrialDeliverySystemDescriptor</b> interface enables the client to get a terrestrial delivery system descriptor from a DVB stream. The terrestrial delivery system descriptor may be present in the network information table (NIT). For more information, refer to ETSI EN 300 468.

## -inheritance

The <b>IDvbTerrestrialDeliverySystemDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDvbTerrestrialDeliverySystemDescriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getnit">IDvbSiParser::GetNIT</a> to get the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvb_nit">IDVB_NIT</a> interface.</li>
<li>Call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvb_nit-getrecorddescriptorbytag">IDVB_NIT::GetRecordDescriptorByTag</a> and pass in the terrestrial delivery system descriptor tag (0x5A). If the descriptor is present, the method returns an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>IDvbTerrestrialDeliverySystemDescriptor</b> interface.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
