---
UID: NN:dvbsiparser.IDVB_ST
title: IDVB_ST (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_ST","IDVB_ST interface [Microsoft TV Technologies]","IDVB_ST interface [Microsoft TV Technologies]","described","IDVB_STInterface","dvbsiparser/IDVB_ST","mstv.idvb_st"]
old-location: mstv\idvb_st.htm
tech.root: mstv
ms.assetid: 56d77564-4de3-4252-9218-a1188f363437
ms.date: 12/05/2018
ms.keywords: IDVB_ST, IDVB_ST interface [Microsoft TV Technologies], IDVB_ST interface [Microsoft TV Technologies],described, IDVB_STInterface, dvbsiparser/IDVB_ST, mstv.idvb_st
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
 - IDVB_ST
 - dvbsiparser/IDVB_ST
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
 - IDVB_ST
---

# IDVB_ST interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_ST</b> interface enables the client to get information from a stuffing table (ST). The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getst">IDvbSiParser::GetST</a> method returns a pointer to this interface.

The purpose of an ST is to invalidate existing table sections when the transport stream crosses the boundary between delivery systems. To invalidate a table section, the section is overwritten with an ST.

## -inheritance

The <b>IDVB_ST</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_ST</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
