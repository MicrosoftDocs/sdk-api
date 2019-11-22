---
UID: NN:atscpsipparser.IATSC_ETT
title: IATSC_ETT (atscpsipparser.h)

description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_ett.htm
tech.root: mstv
ms.assetid: ae52e81e-4de1-480c-82bf-c9629064970c

ms.date: 12/05/2018
ms.keywords: IATSC_ETT, IATSC_ETT interface [Microsoft TV Technologies], IATSC_ETT interface [Microsoft TV Technologies],described, IATSC_ETTInterface, atscpsipparser/IATSC_ETT, mstv.iatsc_ett
ms.topic: interface
f1_keywords: 
 - "atscpsipparser/IATSC_ETT"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IATSC_ETT
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IATSC_ETT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_ETT</b> interface enables the client to get information from an extended text table (ETT). The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatscpsipparser-getett">IAtscPsipParser::GetETT</a> method returns a pointer to this interface.

An ETT provides text descriptions for events or virtual channels. Each ETT contains a single extended text message (ETM) stream. The ETM stream might contain descriptions for multiple languages.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSC_ETT</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IATSC_ETT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSC_ETT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_ett-getetmid">GetEtmId</a>
</td>
<td align="left" width="63%">
Returns the ETM identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_ett-getextendedmessagetext">GetExtendedMessageText</a>
</td>
<td align="left" width="63%">
Returns the message text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_ett-getprotocolversion">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_ett-getversionnumber">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the ETT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iatsc_ett-initialize">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

