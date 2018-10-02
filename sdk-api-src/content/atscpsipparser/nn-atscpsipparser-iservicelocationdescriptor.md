---
UID: NN:atscpsipparser.IServiceLocationDescriptor
title: IServiceLocationDescriptor
author: windows-sdk-content
description: Gets information from the Service Location Descriptor in an Advanced Television Systems Committee (ATSC) Virtual Channel Table (VCT).
old-location: mstv\iservicelocationdescriptor.htm
tech.root: MSTV
ms.assetid: 43dd800b-c51d-4a2f-ad59-943cb4975066
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IServiceLocationDescriptor, IServiceLocationDescriptor interface [Microsoft TV Technologies], IServiceLocationDescriptor interface [Microsoft TV Technologies],described, atscpsipparser/IServiceLocationDescriptor, mstv.iservicelocationdescriptor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IServiceLocationDescriptor interface


## -description


Gets information from the Service Location Descriptor in an Advanced Television Systems Committee  (ATSC) Virtual Channel Table (VCT). The Service Location Descriptor lists the program IDs (PIDs) in an ATSC transport stream. The VCT is a Program and System Information Protocol (PSIP) table that describes the elementary streams for the virtual channels in an ATSC transport stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IServiceLocationDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IServiceLocationDescriptor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8ffc0c58-1305-49bf-bdbd-efb18805516f">GetElementLanguageCode</a>
</td>
<td align="left" width="63%">
Gets a code that identifies the language used for an elementary stream in the transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97b6091b-cacb-4e69-8ca4-c9f4b70f6304">GetElementPID</a>
</td>
<td align="left" width="63%">
Gets the PID that identifies an elementary stream in the transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d95a9af9-2e09-4a94-ac13-1b17698cfff3">GetElementStreamType</a>
</td>
<td align="left" width="63%">
Gets a code that identifies the type of the elementary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/134e4051-6a73-4420-b12d-3171738bd8ad">GetNumberOfElements</a>
</td>
<td align="left" width="63%">
Gets the number of PIDs used for a program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a81a2218-3c44-4b17-a5cb-bb68d10da977">GetPCR_PID</a>
</td>
<td align="left" width="63%">
Gets the program ID (PID) for the packets that contain the Program Clock Reference (PCR) in the transport stream. 

</td>
</tr>
</table> 

