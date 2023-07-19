---
UID: NN:dvbsiparser.IDVB_NIT
title: IDVB_NIT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_NIT","IDVB_NIT interface [Microsoft TV Technologies]","IDVB_NIT interface [Microsoft TV Technologies]","described","IDVB_NITInterface","dvbsiparser/IDVB_NIT","mstv.idvb_nit"]
old-location: mstv\idvb_nit.htm
tech.root: mstv
ms.assetid: 70b638ae-0152-4a44-aeb1-f3ac382c19ce
ms.date: 12/05/2018
ms.keywords: IDVB_NIT, IDVB_NIT interface [Microsoft TV Technologies], IDVB_NIT interface [Microsoft TV Technologies],described, IDVB_NITInterface, dvbsiparser/IDVB_NIT, mstv.idvb_nit
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
 - IDVB_NIT
 - dvbsiparser/IDVB_NIT
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
 - IDVB_NIT
---

# IDVB_NIT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_NIT</b> interface enables the client to get information from a network information table (NIT). The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getnit">IDvbSiParser::GetNIT</a> method returns a pointer to this interface.

A NIT contains information about the network and the physical organization of the transport streams. Because a network typically carries more than one transport stream, the NIT can provide information for tuning and for locating particular transport streams. A NIT carried on one network may contain information about another network.

The original_network_id and transport_stream_id fields together uniquely define a transport stream within the network.

The NIT may contain one or more table-wide descriptors. In addition, each record in the NIT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> or <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> or <b>GetRecordDescriptorByTag</b> method.

## -inheritance

The <b>IDVB_NIT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_NIT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
