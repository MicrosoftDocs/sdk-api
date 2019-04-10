---
UID: NN:atscpsipparser.IATSC_VCT
title: IATSC_VCT (atscpsipparser.h)
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_vct.htm
tech.root: mstv
ms.assetid: 3ff9cd6e-0d25-462c-93a7-2399395f68b0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IATSC_VCT, IATSC_VCT interface [Microsoft TV Technologies], IATSC_VCT interface [Microsoft TV Technologies],described, IATSC_VCTInterface, atscpsipparser/IATSC_VCT, mstv.iatsc_vct
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
 - IATSC_VCT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IATSC_VCT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_VCT</b> interface enables the client to get data from a virtual channel table (VCT). The <a href="https://msdn.microsoft.com/d3df008e-020f-4ed3-9422-2d5f0f0b865f">IAtscPsipParser::GetVCT</a> method returns a pointer to this interface.

A <i>record</i> as defined by this interface corresponds to a virtual channel in the VCT. For example, the <b>GetCountOfRecords</b> method returns the number of virtual channels defined in the VCT.

The VCT may contain one or more table-wide descriptors. In addition, each record in the VCT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> method or the <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> method or the <b>GetRecordDescriptorByTag</b> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSC_VCT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IATSC_VCT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSC_VCT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a6a9f998-f8a8-4459-91f8-aa4a5206d190">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6930490f-235f-40d5-846d-ae9a075c82cc">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of table-wide descriptors in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51bfc546-9150-4063-b8a4-2dc1238070d0">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff875184-1d91-489d-9941-5d1cd3e9e872">GetRecordCarrierFrequency</a>
</td>
<td align="left" width="63%">
Returns the carrier frequency for a channel in this VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d85f653-181f-467f-b278-8bc721f8ff22">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de27ab5f-f3b4-4888-8df0-b8c2efd373d7">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8c975fe-6bf9-443d-b069-cb8e5e01affc">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the VCT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9884a9bd-bd5c-4d6a-a8b0-5ba1406c0210">GetRecordEtmLocation</a>
</td>
<td align="left" width="63%">
Returns the extended text message (ETM) location for a record in the EIT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c94dc694-dc3f-4639-997e-fb6d534c9e4c">GetRecordIsAccessControlledBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the access_controlled bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef02da20-7c81-4c0b-83fd-7e4c0a36ea1a">GetRecordIsHiddenBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the hidden bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74b2ec97-f225-4085-910e-9093995c46f8">GetRecordIsHideGuideBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the hide_guide bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb4dc4f0-2bbb-44f6-b45e-347cce890b75">GetRecordIsOutOfBandBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the out_of_band bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f3e1e5c-0506-420d-981b-d30d77604e97">GetRecordIsPathSelectBitSet</a>
</td>
<td align="left" width="63%">
Queries whether the path_select bit is set for a particular record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/103de5b5-e78c-49a2-81a7-e85eae2d79c1">GetRecordMajorChannelNumber</a>
</td>
<td align="left" width="63%">
Returns the major channel number for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0c6eecb-7543-4476-882c-29b1ee103359">GetRecordMinorChannelNumber</a>
</td>
<td align="left" width="63%">
Returns the minor channel number for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f335414-f37e-4c50-848e-9f3de51f829a">GetRecordModulationMode</a>
</td>
<td align="left" width="63%">
Returns the modulation mode for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b97baa53-d927-4a3c-91a5-3d06d26e797f">GetRecordName</a>
</td>
<td align="left" width="63%">
Returns the name of a specified channel in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11bf3b27-98da-4f4f-a6a9-6c69b20aedda">GetRecordProgramNumber</a>
</td>
<td align="left" width="63%">
Returns the program number for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8975a42e-69f8-43b8-8c02-2f03a4dde29f">GetRecordServiceType</a>
</td>
<td align="left" width="63%">
Returns the service type for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5edc529-ca54-4f18-8859-b7eb168bff0a">GetRecordSourceId</a>
</td>
<td align="left" width="63%">
Returns the source identifier for a record in the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0ecd931-d789-41cd-8056-675e6162a5f1">GetRecordTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the transport stream identifier (TSID) for a specified channel.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/964ae371-e7a5-4278-8408-b39ae4371135">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a table-wide descriptor for the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2ae29f5c-430a-45a0-870e-41b209572775">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the VCT for a table-wide descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c3261e8-c671-48c7-b07c-59ce74b13c76">GetTransportStreamId</a>
</td>
<td align="left" width="63%">
Returns the TSID for the entire VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c89e2fde-958f-4193-84d9-2d98e7560c6a">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the VCT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a127b94-7591-47b4-b631-50a347b540c6">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the object.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

