---
UID: NN:mpeg2psiparser.IPMT
title: IPMT
author: windows-sdk-content
description: The IPMT interface enables the client to get information from a program map table (PMT).
old-location: mstv\ipmt.htm
old-project: mstv
ms.assetid: 0dbd4cc3-5ef3-4c71-ba3f-149d5050ba24
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IPMT, IPMT interface [Microsoft TV Technologies], IPMT interface [Microsoft TV Technologies],described, IPMTInterface, mpeg2psiparser/IPMT, mstv.ipmt
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mpeg2psiparser.h
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
tech.root: 
req.typenames: MPEG_HEADER_VERSION_BITS, *PMPEG_HEADER_VERSION_BITS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mpeg2PsiParser.h
api_name:
 - IPMT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IPMT interface


## -description



The <b>IPMT</b> interface enables the client to get information from a program map table (PMT). The <a href="https://msdn.microsoft.com/cd9a3fb0-4bdc-499b-9db9-85dce50dd24b">IAtscPsipParser::GetPMT</a> method returns a pointer to this interface.

The PMT may contain one or more table-wide descriptors. In addition, each record in the PMT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> or <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> or <b>GetRecordDescriptorByTag</b> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPMT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPMT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPMT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc3eb6f3-c539-42c4-847a-5d1e80c53255">ConvertNextToCurrent</a>
</td>
<td align="left" width="63%">
Converts a <i>next</i> table to a <i>current</i> table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4e5009b-4c0d-4d0c-b480-4030cedbdb97">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1f91a13-afec-4703-8f1c-be64c8a8b8f9">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of table-wide descriptors in the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1e6f321-b24b-46dc-8da8-5a4bbda61918">GetNextTable</a>
</td>
<td align="left" width="63%">
Retrieves the <i>next</i> table that follows the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0099e5b3-d573-47b9-9581-fbb9fee3ca16">GetPcrPid</a>
</td>
<td align="left" width="63%">
Returns the packet identifier (PID) of the packets that contain the Program Clock Reference (PCR) fields for this program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39006f8b-7dd4-4f19-badc-3a288a7b6520">GetProgramNumber</a>
</td>
<td align="left" width="63%">
Returns the program number for the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2470267-25a6-4ed3-91a1-30fd3ac7bbea">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e37db4b-1b86-4b34-8f93-642bb603789e">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a descriptor for a specified record in the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ed3dd22-331a-419a-ab30-5645e259e36a">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the PMT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed4790ee-97ce-482e-834e-4081a310f4bb">GetRecordElementaryPid</a>
</td>
<td align="left" width="63%">
Returns the PID for a given elementary stream in the program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3e17c0c-88ea-4143-aa9b-da2c5bf2069f">GetRecordStreamType</a>
</td>
<td align="left" width="63%">
Returns the stream type for a given elementary stream in the program.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31442c1f-0921-49b8-ab38-d75ccc2c4f0e">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Retrieves a table-wide descriptor for the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e70bcffb-41ea-4f25-bb93-dc43339ae6ba">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the PMT for a table-wide descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00385ea4-27a9-47f4-91af-22fa82d83668">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the PMT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14611397-7885-4553-905e-db56404f5e97">QueryMPEInfo</a>
</td>
<td align="left" width="63%">
Returns the Multi-Protocol Encapsulation (MPE) information in the PMT, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fead4140-5585-44eb-9d1f-7a686b79ac26">QueryServiceGatewayInfo</a>
</td>
<td align="left" width="63%">
Returns the DSM-CC service gateway information in the PMT, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6794c94a-8efe-4d53-a4f4-e25d14644270">RegisterForNextTable</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when a <i>next</i> table arrives that will replace the current table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4759c813-3a1f-492a-bca9-cb6610f6426b">RegisterForWhenCurrent</a>
</td>
<td align="left" width="63%">
Registers the client to be notified when the table becomes current.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

