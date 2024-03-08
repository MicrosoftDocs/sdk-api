---
UID: NN:dvbsiparser.IISDB_BIT
title: IISDB_BIT (dvbsiparser.h)
description: Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT). A BIT contains a broadcaster unit and the service information transmission parameter for each broadcaster unit.
helpviewer_keywords: ["IISDB_BIT","IISDB_BIT interface [Microsoft TV Technologies]","IISDB_BIT interface [Microsoft TV Technologies]","described","dvbsiparser/IISDB_BIT","mstv.iisdb_bit"]
old-location: mstv\iisdb_bit.htm
tech.root: mstv
ms.assetid: 0ec4497c-68c3-4b0e-a9e4-332e42b2c89b
ms.date: 12/05/2018
ms.keywords: IISDB_BIT, IISDB_BIT interface [Microsoft TV Technologies], IISDB_BIT interface [Microsoft TV Technologies],described, dvbsiparser/IISDB_BIT, mstv.iisdb_bit
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
 - IISDB_BIT
 - dvbsiparser/IISDB_BIT
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
 - IISDB_BIT
---

# IISDB_BIT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Implements methods that get information from an Integrated Services Digital Broadcasting (ISDB) broadcaster information table (BIT). A BIT contains a broadcaster unit and the service information transmission parameter
  for each broadcaster unit.


To obtain a pointer to this interface, first make sure that the media graph is in a running state and that the stream you are tuned to contains a BIT. Then:

<ol>
<li>Query the <a href="/previous-versions/windows/desktop/mstv/bda-mpeg-2-transport-information-filter">BDA MPEG-2 Transport Information Filter</a> to obtain a pointer to the <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-ipsitables">IPSITables</a> interface. (You can also go through the graph and query each filter until you find one that supports <b>IPSITables</b>.)</li>
<li>Call the <a href="/windows/desktop/api/mpeg2psiparser/nf-mpeg2psiparser-ipsitables-gettable">IPSITables::GetTable</a> method. The interface pointer for the desired table is returned in the <i>ppIUnknown</i> output parameter.
</li>
</ol>

## -inheritance

The <b>IISDB_BIT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IISDB_BIT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

