---
UID: NN:dvbsiparser.IISDB_EMM
title: IISDB_EMM (dvbsiparser.h)
description: Gets data from an Integrated Services Digital Broadcasting (ISDB) entitlement management message (EMM) table.
helpviewer_keywords: ["IISDB_EMM","IISDB_EMM interface [Microsoft TV Technologies]","IISDB_EMM interface [Microsoft TV Technologies]","described","dvbsiparser/IISDB_EMM","mstv.iisdb_emm"]
old-location: mstv\iisdb_emm.htm
tech.root: mstv
ms.assetid: a1389e7c-a3f1-4782-b811-5e09615b3e47
ms.date: 12/05/2018
ms.keywords: IISDB_EMM, IISDB_EMM interface [Microsoft TV Technologies], IISDB_EMM interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_EMM, mstv.iisdb_emm
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
 - IISDB_EMM
 - dvbsiparser/IISDB_EMM
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
 - IISDB_EMM
---

# IISDB_EMM interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets data from an Integrated Services Digital Broadcasting (ISDB)
  entitlement management message (EMM) table. An EMM table contains conditional access data, including contract
  information for subscribers, keys to decrypt common information, and the
  authorization levels or services of specific decoders.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an EMM. Then:

<ol>
<li>Query the <a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>

## -inheritance

The <b>IISDB_EMM</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IISDB_EMM</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

