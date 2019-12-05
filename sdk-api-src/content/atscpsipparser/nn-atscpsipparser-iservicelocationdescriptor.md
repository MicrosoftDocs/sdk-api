---
UID: NN:atscpsipparser.IServiceLocationDescriptor
title: IServiceLocationDescriptor (atscpsipparser.h)
description: Gets information from the Service Location Descriptor in an Advanced Television Systems Committee (ATSC) Virtual Channel Table (VCT).
old-location: mstv\iservicelocationdescriptor.htm
tech.root: mstv
ms.assetid: 43dd800b-c51d-4a2f-ad59-943cb4975066
ms.date: 12/05/2018
ms.keywords: IServiceLocationDescriptor, IServiceLocationDescriptor interface [Microsoft TV Technologies], IServiceLocationDescriptor interface [Microsoft TV Technologies],described, atscpsipparser/IServiceLocationDescriptor, mstv.iservicelocationdescriptor
ms.topic: interface
f1_keywords:
- atscpsipparser/IServiceLocationDescriptor
dev_langs:
- c++
req.header: atscpsipparser.h
req.include-header: Atscpsipparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- atscpsipparser.h
api_name:
- IServiceLocationDescriptor
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IServiceLocationDescriptor interface


## -description


Gets information from the Service Location Descriptor in an Advanced Television Systems Committee  (ATSC) Virtual Channel Table (VCT). The Service Location Descriptor lists the program IDs (PIDs) in an ATSC transport stream. The VCT is a Program and System Information Protocol (PSIP) table that describes the elementary streams for the virtual channels in an ATSC transport stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceLocationDescriptor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IServiceLocationDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IServiceLocationDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iservicelocationdescriptor-getelementlanguagecode">GetElementLanguageCode</a>
</td>
<td align="left" width="63%">
Gets a code that identifies the language used for an elementary stream in the transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iservicelocationdescriptor-getelementpid">GetElementPID</a>
</td>
<td align="left" width="63%">
Gets the PID that identifies an elementary stream in the transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iservicelocationdescriptor-getelementstreamtype">GetElementStreamType</a>
</td>
<td align="left" width="63%">
Gets a code that identifies the type of the elementary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iservicelocationdescriptor-getnumberofelements">GetNumberOfElements</a>
</td>
<td align="left" width="63%">
Gets the number of PIDs used for a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iservicelocationdescriptor-getpcr_pid">GetPCR_PID</a>
</td>
<td align="left" width="63%">
Gets the program ID (PID) for the packets that contain the Program Clock Reference (PCR) in the transport stream. 

</td>
</tr>
</table> 

