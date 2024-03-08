---
UID: NN:atscpsipparser.ISCTE_EAS
title: ISCTE_EAS (atscpsipparser.h)
description: The ISCTE_EAS interface enables the client to get data from an ATSC emergency alert message (EAS) table.
helpviewer_keywords: ["ISCTE_EAS","ISCTE_EAS interface [Microsoft TV Technologies]","ISCTE_EAS interface [Microsoft TV Technologies]","described","ISCTE_EASInterface","atscpsipparser/ISCTE_EAS","mstv.iscte_eas"]
old-location: mstv\iscte_eas.htm
tech.root: mstv
ms.assetid: 7b5620c3-f460-4118-a8a2-9b2561bd12cf
ms.date: 12/05/2018
ms.keywords: ISCTE_EAS, ISCTE_EAS interface [Microsoft TV Technologies], ISCTE_EAS interface [Microsoft TV Technologies],described, ISCTE_EASInterface, atscpsipparser/ISCTE_EAS, mstv.iscte_eas
req.header: atscpsipparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
 - ISCTE_EAS
 - atscpsipparser/ISCTE_EAS
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
 - ISCTE_EAS
---

# ISCTE_EAS interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ISCTE_EAS</b> interface enables the client to get data from an ATSC emergency alert message (EAS) table. The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-geteas">IAtscPsipParser::GetEAS</a> method returns a pointer to this interface.

For more information about EAS tables, see ANSI-J-STD-042-A, Emergency Alert Message for Cable.

## -inheritance

The <b>ISCTE_EAS</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISCTE_EAS</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
