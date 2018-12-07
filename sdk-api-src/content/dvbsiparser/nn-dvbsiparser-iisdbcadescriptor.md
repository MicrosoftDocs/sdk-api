---
UID: NN:dvbsiparser.IIsdbCADescriptor
title: IIsdbCADescriptor
author: windows-sdk-content
description: Implements methods that get data from an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) descriptor.
old-location: mstv\iisdbcadescriptor.htm
tech.root: mstv
ms.assetid: 6683f3db-636b-42bb-a46d-c175a4324023
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IIsdbCADescriptor, IIsdbCADescriptor interface [Microsoft TV Technologies], IIsdbCADescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IIsdbCADescriptor, mstv.iisdbcadescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - dvbsiparser.h
api_name:
 - IIsdbCADescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IIsdbCADescriptor interface


## -description


 Implements methods that get data from  an Integrated Services Digital Broadcasting (ISDB) conditional access (CA) descriptor. The CA descriptor appears in the ISDB service information as part of the conditional access table (CAT) or program map table (PMT) and indicates the program identifiers (PIDs) of transport stream packets that contain entitlement control message (ECM) data or entitlement management message (EMM) data.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IIsdbCADescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IIsdbCADescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IIsdbCADescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9d4815f2-7f58-4952-a64b-067c99ae8d43">GetCAPID</a>
</td>
<td align="left" width="63%">
Gets the CA  program identifier (PID) from an ISDB CA descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/834825d4-f92d-4cca-bf15-a3f94647c4f1">GetCASystemId</a>
</td>
<td align="left" width="63%">
Gets the conditional-access system identifier from an ISDB CA descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25331811-51d4-4009-8fc2-825a8de33dcf">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of an ISDB conditional access descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd64ba74-aab2-45eb-945a-187d3aaf9bdd">GetPrivateDataBytes</a>
</td>
<td align="left" width="63%">
Gets private data bytes from an ISDB CA descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c45295f9-df77-4a23-b6c2-65d5b2c9c360">GetReservedBits</a>
</td>
<td align="left" width="63%">
Gets the reserved bits from an ISDB CA descriptor. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8ed1538-3540-42c2-a465-ab6d580b0b31">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies an ISDB CA descriptor.

</td>
</tr>
</table> 

