---
UID: NN:dvbsiparser.IDVB_SIT
title: IDVB_SIT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_SIT","IDVB_SIT interface [Microsoft TV Technologies]","IDVB_SIT interface [Microsoft TV Technologies]","described","IDVB_SITInterface","dvbsiparser/IDVB_SIT","mstv.idvb_sit"]
old-location: mstv\idvb_sit.htm
tech.root: mstv
ms.assetid: f278d942-a450-4a01-998d-4dac1c8a1fcc
ms.date: 12/05/2018
ms.keywords: IDVB_SIT, IDVB_SIT interface [Microsoft TV Technologies], IDVB_SIT interface [Microsoft TV Technologies],described, IDVB_SITInterface, dvbsiparser/IDVB_SIT, mstv.idvb_sit
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
 - IDVB_SIT
 - dvbsiparser/IDVB_SIT
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
 - IDVB_SIT
---

# IDVB_SIT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_SIT</b> interface enables the client to get information from a selection information table (SIT). The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getsit">IDvbSiParser::GetSIT</a> method returns a pointer to this interface.

The presence of a SIT in a transport stream indicates that the transport stream is <i>partial</i>, meaning the stream contains a subset of a complete broadcast stream. A partial transport stream does not carry any service information (SI) tables other than SITs and discontinuity information tables (DITs). The SIT contains a summary of the full SI information for the stream.

The SIT may contain one or more table-wide descriptors. In addition, each record in the SIT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> or <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> or <b>GetRecordDescriptorByTag</b> method.

## -inheritance

The <b>IDVB_SIT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_SIT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
