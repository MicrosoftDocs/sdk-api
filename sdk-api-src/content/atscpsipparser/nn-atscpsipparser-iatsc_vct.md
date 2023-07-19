---
UID: NN:atscpsipparser.IATSC_VCT
title: IATSC_VCT (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IATSC_VCT","IATSC_VCT interface [Microsoft TV Technologies]","IATSC_VCT interface [Microsoft TV Technologies]","described","IATSC_VCTInterface","atscpsipparser/IATSC_VCT","mstv.iatsc_vct"]
old-location: mstv\iatsc_vct.htm
tech.root: mstv
ms.assetid: 3ff9cd6e-0d25-462c-93a7-2399395f68b0
ms.date: 12/05/2018
ms.keywords: IATSC_VCT, IATSC_VCT interface [Microsoft TV Technologies], IATSC_VCT interface [Microsoft TV Technologies],described, IATSC_VCTInterface, atscpsipparser/IATSC_VCT, mstv.iatsc_vct
req.header: atscpsipparser.h
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
 - IATSC_VCT
 - atscpsipparser/IATSC_VCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_VCT
---

# IATSC_VCT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_VCT</b> interface enables the client to get data from a virtual channel table (VCT). The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getvct">IAtscPsipParser::GetVCT</a> method returns a pointer to this interface.

A <i>record</i> as defined by this interface corresponds to a virtual channel in the VCT. For example, the <b>GetCountOfRecords</b> method returns the number of virtual channels defined in the VCT.

The VCT may contain one or more table-wide descriptors. In addition, each record in the VCT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> method or the <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> method or the <b>GetRecordDescriptorByTag</b> method.

## -inheritance

The <b>IATSC_VCT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IATSC_VCT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
