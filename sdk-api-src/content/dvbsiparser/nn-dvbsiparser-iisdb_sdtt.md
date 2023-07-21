---
UID: NN:dvbsiparser.IISDB_SDTT
title: IISDB_SDTT (dvbsiparser.h)
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) software download trigger table (SDTT). An SDTT contains download information such as service ID, schedule, and receiver types for revision.
helpviewer_keywords: ["IISDB_SDTT","IISDB_SDTT interface [Microsoft TV Technologies]","IISDB_SDTT interface [Microsoft TV Technologies]","described","dvbsiparser/IISDB_SDTT","mstv.iisdb_sdtt"]
old-location: mstv\iisdb_sdtt.htm
tech.root: mstv
ms.assetid: f6ed35bc-4470-4000-8f0d-19d454453720
ms.date: 12/05/2018
ms.keywords: IISDB_SDTT, IISDB_SDTT interface [Microsoft TV Technologies], IISDB_SDTT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_SDTT, mstv.iisdb_sdtt
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
 - IISDB_SDTT
 - dvbsiparser/IISDB_SDTT
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
 - IISDB_SDTT
---

# IISDB_SDTT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that get data
  from an Integrated Services Digital Broadcasting (ISDB)  software download
  trigger table
  (SDTT). An SDTT contains download information such as service ID, schedule, and
  receiver types for revision.

To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains an SDTT. Then:

<ol>
<li>Query the <a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>

## -inheritance

The <b>IISDB_SDTT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IISDB_SDTT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

