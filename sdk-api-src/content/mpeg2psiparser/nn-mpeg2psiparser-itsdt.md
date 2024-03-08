---
UID: NN:mpeg2psiparser.ITSDT
title: ITSDT (mpeg2psiparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
helpviewer_keywords: ["ITSDT","ITSDT interface [Microsoft TV Technologies]","ITSDT interface [Microsoft TV Technologies]","described","ITSDTInterface","mpeg2psiparser/ITSDT","mstv.itsdt"]
old-location: mstv\itsdt.htm
tech.root: mstv
ms.assetid: 58ec73dc-79bd-415b-b9be-8e9246166391
ms.date: 12/05/2018
ms.keywords: ITSDT, ITSDT interface [Microsoft TV Technologies], ITSDT interface [Microsoft TV Technologies],described, ITSDTInterface, mpeg2psiparser/ITSDT, mstv.itsdt
req.header: mpeg2psiparser.h
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
 - ITSDT
 - mpeg2psiparser/ITSDT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - ITSDT
---

# ITSDT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005.
        

The <b>ITSDT</b> interface enables the client to get data from a transport stream description table (TSDT). The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-gettsdt">IAtscPsipParser::GetTSDT</a> and <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbsiparser-gettsdt">IDvbSiParser::GetTSDT</a> methods return pointers to this interface.

## -inheritance

The <b>ITSDT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITSDT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
