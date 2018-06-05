---
UID: NN:atscpsipparser.IATSC_MGT
title: IATSC_MGT
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsc_mgt.htm
old-project: mstv
ms.assetid: 2d6cc17f-7288-468c-a028-31e6e284d8ca
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IATSC_MGT, IATSC_MGT interface [Microsoft TV Technologies], IATSC_MGT interface [Microsoft TV Technologies],described, IATSC_MGTInterface, atscpsipparser/IATSC_MGT, mstv.iatsc_mgt
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	IATSC_MGT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IATSC_MGT interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IATSC_MGT</b> interface enables the client to get data from a master guide table (MGT). The MGT describes the program guide information and service information that is delivered in a transport stream, including the table types, the packet identifiers, and the version numbers. The <a href="https://msdn.microsoft.com/abdfb558-aab9-4929-822a-08b35235c22f">IAtscPsipParser::GetMGT</a> method returns a pointer to this interface.

The MGT may contain one or more table-wide descriptors. In addition, each record in the MGT may have one or more descriptors. To get the table-wide descriptors, use the <b>GetTableDescriptorByIndex</b> method or the <b>GetTableDescriptorByTag</b> method. To get the record descriptors, use the <b>GetRecordDescriptorByIndex</b> method or the <b>GetRecordDescriptorByTag</b> method.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IATSC_MGT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IATSC_MGT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IATSC_MGT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f0c7f28-3280-4c2a-a030-68326eac23f0">GetCountOfRecords</a>
</td>
<td align="left" width="63%">
Returns the number of records in the MGT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14bd596f-ca24-456b-bb53-4e7e37183422">GetCountOfTableDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of table-wide descriptors in the MGT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c4d7087-d867-4ced-9bb4-c3a0f521fa72">GetProtocolVersion</a>
</td>
<td align="left" width="63%">
Returns the protocol version of the table.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66be731b-d964-4806-ae78-2faa0c0d2810">GetRecordCountOfDescriptors</a>
</td>
<td align="left" width="63%">
Returns the number of descriptors for a record in the MGT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/87a37141-6426-4f75-b5c5-f39e05262060">GetRecordDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a descriptor for a specified record in the MGT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fcc309ca-05bb-45cf-8930-f4413f84a55c">GetRecordDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches a record in the MGT for a descriptor with a specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f3a1ef39-7de4-4979-acb9-805893f41937">GetRecordType</a>
</td>
<td align="left" width="63%">
Returns the table type for a record in the MGT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8c4cfba-b03c-478e-a49e-c01d663535a0">GetRecordTypePid</a>
</td>
<td align="left" width="63%">
Returns the packet identifier (PID) for the table type described by a record in the MGT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a5ec8e9-d1e6-4514-8d0d-7992be52ba8c">GetRecordVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the table type described by a record in the MGT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4cf36ca4-0bc2-401e-a6f2-be23d64a1af6">GetTableDescriptorByIndex</a>
</td>
<td align="left" width="63%">
Returns a table-wide descriptor for the MGT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fd12c9b-fa63-4463-a8ef-a4c38e008d65">GetTableDescriptorByTag</a>
</td>
<td align="left" width="63%">
Searches the MGT for a table-wide descriptor with the specified descriptor tag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5bfc7ca8-543d-4222-9c0a-effbed7d39e8">GetVersionNumber</a>
</td>
<td align="left" width="63%">
Returns the version number for the MGT.

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
</table> 


## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

