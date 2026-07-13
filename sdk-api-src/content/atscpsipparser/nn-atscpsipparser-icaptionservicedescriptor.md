---
UID: NN:atscpsipparser.ICaptionServiceDescriptor
title: ICaptionServiceDescriptor (atscpsipparser.h)
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
helpviewer_keywords: ["ICaptionServiceDescriptor","ICaptionServiceDescriptor interface [Microsoft TV Technologies]","ICaptionServiceDescriptor interface [Microsoft TV Technologies]","described","ICaptionServiceDescriptorInterface","atscpsipparser/ICaptionServiceDescriptor","mstv.icaptionservicedescriptor"]
old-location: mstv\icaptionservicedescriptor.htm
tech.root: mstv
ms.assetid: fc1f38af-2fe8-4c08-b6f8-312dd4771141
ms.date: 12/05/2018
ms.keywords: ICaptionServiceDescriptor, ICaptionServiceDescriptor interface [Microsoft TV Technologies], ICaptionServiceDescriptor interface [Microsoft TV Technologies],described, ICaptionServiceDescriptorInterface, atscpsipparser/ICaptionServiceDescriptor, mstv.icaptionservicedescriptor
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
 - ICaptionServiceDescriptor
 - atscpsipparser/ICaptionServiceDescriptor
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
 - ICaptionServiceDescriptor
---

# ICaptionServiceDescriptor interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>ICaptionServiceDescriptor</b> interface enables the client to get caption service descriptors from a Program and System Information Protocol (PSIP) table in an ATSC stream. The content advisor descriptor may be present in the event information table (EIT). For more information, refer to ATSC Standard A/65B, Program and System Information Protocol for Terrestrial Broadcast and Cable (Revision B).

## -inheritance

The <b>ICaptionServiceDescriptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICaptionServiceDescriptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-geteit">IAtscPsipParser::GetEIT</a> to get the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iatsc_eit">IATSC_EIT</a> interface.</li>
<li>Call <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_eit-getrecorddescriptorbytag">IATSC_EIT::GetRecordDescriptorByTag</a> and pass in the caption service descriptor tag (0x86). If the descriptor is present, the method returns an <a href="/windows/desktop/api/mpeg2psiparser/nn-mpeg2psiparser-igenericdescriptor">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>ICaptionServiceDescriptor</b> interface.</li>
</ol>

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
