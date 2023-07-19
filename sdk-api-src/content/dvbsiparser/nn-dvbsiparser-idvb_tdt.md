---
UID: NN:dvbsiparser.IDVB_TDT
title: IDVB_TDT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_TDT","IDVB_TDT interface [Microsoft TV Technologies]","IDVB_TDT interface [Microsoft TV Technologies]","described","IDVB_TDTInterface","dvbsiparser/IDVB_TDT","mstv.idvb_tdt"]
old-location: mstv\idvb_tdt.htm
tech.root: mstv
ms.assetid: 15fed2d3-fcc8-4992-9dff-4cd5f617e55b
ms.date: 12/05/2018
ms.keywords: IDVB_TDT, IDVB_TDT interface [Microsoft TV Technologies], IDVB_TDT interface [Microsoft TV Technologies],described, IDVB_TDTInterface, dvbsiparser/IDVB_TDT, mstv.idvb_tdt
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
 - IDVB_TDT
 - dvbsiparser/IDVB_TDT
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
 - IDVB_TDT
---

# IDVB_TDT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_TDT</b> interface enables the client to get information from a time and date table (TDT). The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-gettdt">IDvbSiParser::GetTDT</a> method returns a pointer to this interface. The TDT provides the current time and date, in Universal Time Coordinated (UTC) format.

## -inheritance

The <b>IDVB_TDT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_TDT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
