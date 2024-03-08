---
UID: NN:mpeg2psiparser.IPMT
title: IPMT (mpeg2psiparser.h)
description: The IPMT interface enables the client to get information from a program map table (PMT).
helpviewer_keywords: ["IPMT","IPMT interface [Microsoft TV Technologies]","IPMT interface [Microsoft TV Technologies]","described","IPMTInterface","mpeg2psiparser/IPMT","mstv.ipmt"]
old-location: mstv\ipmt.htm
tech.root: mstv
ms.assetid: 0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24
ms.date: 12/05/2018
ms.keywords: IPMT, IPMT interface [Microsoft TV Technologies], IPMT interface [Microsoft TV Technologies],described, IPMTInterface, mpeg2psiparser/IPMT, mstv.ipmt
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
 - IPMT
 - mpeg2psiparser/IPMT
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
 - IPMT
---

# IPMT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IPMT</b> interface enables the client to get information from a program map table (PMT). The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getpmt">IAtscPsipParser::GetPMT</a> method returns a pointer to this interface.

The PMT may contain one or more table-wide descriptors. In addition, each record in the PMT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> or <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> or <b>GetRecordDescriptorByTag</b> method.

## -inheritance

The <b>IPMT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPMT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
