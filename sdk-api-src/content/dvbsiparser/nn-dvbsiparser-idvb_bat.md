---
UID: NN:dvbsiparser.IDVB_BAT
title: IDVB_BAT (dvbsiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IDVB_BAT","IDVB_BAT interface [Microsoft TV Technologies]","IDVB_BAT interface [Microsoft TV Technologies]","described","IDVB_BATInterface","dvbsiparser/IDVB_BAT","mstv.idvb_bat"]
old-location: mstv\idvb_bat.htm
tech.root: mstv
ms.assetid: c312a152-21ee-4708-90a8-ab9bde9a2011
ms.date: 12/05/2018
ms.keywords: IDVB_BAT, IDVB_BAT interface [Microsoft TV Technologies], IDVB_BAT interface [Microsoft TV Technologies],described, IDVB_BATInterface, dvbsiparser/IDVB_BAT, mstv.idvb_bat
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
 - IDVB_BAT
 - dvbsiparser/IDVB_BAT
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
 - IDVB_BAT
---

# IDVB_BAT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IDVB_BAT</b> interface enables the client to get data from a bouquet association table (BAT). The <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-getbat">IDvbSiParser::GetBAT</a> method returns a pointer to this interface.

A bouquet is a collection of services that are marketed as one entity. A single bouquet may contain several transport streams that are delivered across different distribution media (satellite, cable, or terrestrial).

The BAT may contain one or more table-wide descriptors. In addition, each record in the BAT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> or <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> or <b>GetRecordDescriptorByTag</b> method.

## -inheritance

The <b>IDVB_BAT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDVB_BAT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
