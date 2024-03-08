---
UID: NN:dvbsiparser.IDVB_TOT
title: IDVB_TOT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_TOT","IDVB_TOT interface [Microsoft TV Technologies]","IDVB_TOT interface [Microsoft TV Technologies]","described","IDVB_TOTInterface","dvbsiparser/IDVB_TOT","mstv.idvb_tot"]
old-location: mstv\idvb_tot.htm
tech.root: mstv
ms.assetid: fe5b6b7c-fc6b-4889-b780-4b9f61f3e895
ms.date: 12/05/2018
ms.keywords: IDVB_TOT, IDVB_TOT interface [Microsoft TV Technologies], IDVB_TOT interface [Microsoft TV Technologies],described, IDVB_TOTInterface, dvbsiparser/IDVB_TOT, mstv.idvb_tot
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
 - IDVB_TOT
 - dvbsiparser/IDVB_TOT
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
 - IDVB_TOT
---

# IDVB_TOT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_TOT</b> interface enables the client to get information from a time offset table (TOT). The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-gettot">IDvbSiParser::GetTOT</a> method returns a pointer to this information. A TOT contains the current UTC time, plus the offset from UTC for local time in one or more regions. The offsets are contained in a <i>local offset time descriptor</i>, as specified by ETSI EN 300 468.

## -inheritance

The <b>IDVB_TOT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_TOT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
