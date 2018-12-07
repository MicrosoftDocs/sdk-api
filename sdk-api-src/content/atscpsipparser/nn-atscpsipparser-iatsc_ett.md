---
UID: NN:atscpsipparser.IATSC_ETT
title: IATSC_ETT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_ett.htm
tech.root: mstv
ms.assetid: ae52e81e-4de1-480c-82bf-c9629064970c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IATSC_ETT, IATSC_ETT interface [Microsoft TV Technologies], IATSC_ETT interface [Microsoft TV Technologies],described, IATSC_ETTInterface, atscpsipparser/IATSC_ETT, mstv.iatsc_ett
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSC_ETT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_ETT</b> interface enables the client to get information from an extended text table (ETT). The <a href="https://msdn.microsoft.com/6838620a-3dee-468e-bfc8-00757c06263e">IAtscPsipParser::GetETT</a> method returns a pointer to this interface.

An ETT provides text descriptions for events or virtual channels. Each ETT contains a single extended text message (ETM) stream. The ETM stream might contain descriptions for multiple languages.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSC_ETT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IATSC_ETT</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/e45e6709-bb16-4644-b2d1-2ffd6d85f224">GetEtmId</a>
</td>
<td align="left" width="63%">
Returns the ETM identifier.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4e1b5f65-4662-41aa-8a11-cce6a2debb9e">GetExtendedMessageText</a>
</td>
<td align="left" width="63%">
Returns the message text.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fc7673c-486a-48dc-a283-55fbef42a2b0">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd9eefda-51ff-472c-b363-2f3c21ae2fec">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the ETT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2278b4e0-f30d-4405-a05b-8cd93b1de185">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

