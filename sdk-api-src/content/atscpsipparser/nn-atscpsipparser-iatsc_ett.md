---
UID: NN:atscpsipparser.IATSC_ETT
title: IATSC_ETT (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["IATSC_ETT","IATSC_ETT interface [Microsoft TV Technologies]","IATSC_ETT interface [Microsoft TV Technologies]","described","IATSC_ETTInterface","atscpsipparser/IATSC_ETT","mstv.iatsc_ett"]
old-location: mstv\iatsc_ett.htm
tech.root: mstv
ms.assetid: ae52e81e-4de1-480c-82bf-c9629064970c
ms.date: 12/05/2018
ms.keywords: IATSC_ETT, IATSC_ETT interface [Microsoft TV Technologies], IATSC_ETT interface [Microsoft TV Technologies],described, IATSC_ETTInterface, atscpsipparser/IATSC_ETT, mstv.iatsc_ett
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
 - IATSC_ETT
 - atscpsipparser/IATSC_ETT
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
 - IATSC_ETT
---

# IATSC_ETT interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_ETT</b> interface enables the client to get information from an extended text table (ETT). The <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getett">IAtscPsipParser::GetETT</a> method returns a pointer to this interface.

An ETT provides text descriptions for events or virtual channels. Each ETT contains a single extended text message (ETM) stream. The ETM stream might contain descriptions for multiple languages.

## -inheritance

The <b>IATSC_ETT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IATSC_ETT</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
