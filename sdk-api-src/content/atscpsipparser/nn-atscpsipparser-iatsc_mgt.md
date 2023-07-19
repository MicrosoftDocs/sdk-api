---
UID: NN:atscpsipparser.IATSC_MGT
title: IATSC_MGT (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IATSC_MGT","IATSC_MGT interface [Microsoft TV Technologies]","IATSC_MGT interface [Microsoft TV Technologies]","described","IATSC_MGTInterface","atscpsipparser/IATSC_MGT","mstv.iatsc_mgt"]
old-location: mstv\iatsc_mgt.htm
tech.root: mstv
ms.assetid: 2d6cc17f-7288-468c-a028-31e6e284d8ca
ms.date: 12/05/2018
ms.keywords: IATSC_MGT, IATSC_MGT interface [Microsoft TV Technologies], IATSC_MGT interface [Microsoft TV Technologies],described, IATSC_MGTInterface, atscpsipparser/IATSC_MGT, mstv.iatsc_mgt
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
 - IATSC_MGT
 - atscpsipparser/IATSC_MGT
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
 - IATSC_MGT
---

# IATSC_MGT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_MGT</b> interface enables the client to get data from a master guide table (MGT). The MGT describes the program guide information and service information that is delivered in a transport stream, including the table types, the packet identifiers, and the version numbers. The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getmgt">IAtscPsipParser::GetMGT</a> method returns a pointer to this interface.

The MGT may contain one or more table-wide descriptors. In addition, each record in the MGT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> method or the <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> method or the <b>GetRecordDescriptorByTag</b> method.

## -inheritance

The <b>IATSC_MGT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IATSC_MGT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
