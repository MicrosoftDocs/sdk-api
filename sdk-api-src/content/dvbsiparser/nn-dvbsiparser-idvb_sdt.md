---
UID: NN:dvbsiparser.IDVB_SDT
title: IDVB_SDT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_SDT","IDVB_SDT interface [Microsoft TV Technologies]","IDVB_SDT interface [Microsoft TV Technologies]","described","IDVB_SDTInterface","dvbsiparser/IDVB_SDT","mstv.idvb_sdt"]
old-location: mstv\idvb_sdt.htm
tech.root: mstv
ms.assetid: bb473a7e-8957-4e85-98d0-13c6992fbf37
ms.date: 12/05/2018
ms.keywords: IDVB_SDT, IDVB_SDT interface [Microsoft TV Technologies], IDVB_SDT interface [Microsoft TV Technologies],described, IDVB_SDTInterface, dvbsiparser/IDVB_SDT, mstv.idvb_sdt
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
 - IDVB_SDT
 - dvbsiparser/IDVB_SDT
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
 - IDVB_SDT
---

# IDVB_SDT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_SDT</b> interface enables the client to get information from a service description table (SDT). The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getsdt">IDvbSiParser::GetSDT</a> method returns a pointer to this interface.

An SDT describes one or more services that are carried in a particular transport stream. The services may be carried in the same transport stream that carries the SDT, or a different transport stream.

## -inheritance

The <b>IDVB_SDT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_SDT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
