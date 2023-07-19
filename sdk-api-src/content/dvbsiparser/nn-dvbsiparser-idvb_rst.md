---
UID: NN:dvbsiparser.IDVB_RST
title: IDVB_RST (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_RST","IDVB_RST interface [Microsoft TV Technologies]","IDVB_RST interface [Microsoft TV Technologies]","described","IDVB_RSTInterface","dvbsiparser/IDVB_RST","mstv.idvb_rst"]
old-location: mstv\idvb_rst.htm
tech.root: mstv
ms.assetid: deee44cb-92b8-4d10-91d7-c99324ab5832
ms.date: 12/05/2018
ms.keywords: IDVB_RST, IDVB_RST interface [Microsoft TV Technologies], IDVB_RST interface [Microsoft TV Technologies],described, IDVB_RSTInterface, dvbsiparser/IDVB_RST, mstv.idvb_rst
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
 - IDVB_RST
 - dvbsiparser/IDVB_RST
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
 - IDVB_RST
---

# IDVB_RST interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_RST</b> interface enables the client to get information from a running status table (RST). The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getrst">IDvbSiParser::GetRST</a> method returns a pointer to this interface. The RST enables the provider to update the timing status for one or more events, which may be needed if the schedule changes.

## -inheritance

The <b>IDVB_RST</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_RST</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
