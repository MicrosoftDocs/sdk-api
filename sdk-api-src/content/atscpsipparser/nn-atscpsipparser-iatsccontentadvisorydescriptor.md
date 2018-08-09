---
UID: NN:atscpsipparser.IAtscContentAdvisoryDescriptor
title: IAtscContentAdvisoryDescriptor
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\iatsccontentadvisorydescriptor.htm
old-project: mstv
ms.assetid: b7379d66-c57b-45e0-9c63-901bf3637f21
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IAtscContentAdvisoryDescriptor, IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies], IAtscContentAdvisoryDescriptor interface [Microsoft TV Technologies],described, IAtscContentAdvisoryDescriptorInterface, atscpsipparser/IAtscContentAdvisoryDescriptor, mstv.iatsccontentadvisorydescriptor
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
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IAtscContentAdvisoryDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAtscContentAdvisoryDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>IAtscContentAdvisoryDescriptor</b> interface enables the client to get a content advisory descriptor from a Program and System Information Protocol (PSIP) table in an ATSC stream. The content advisor descriptor may be present in the event information table (EIT). For more information, refer to ATSC Standard A/65B, Program and System Information Protocol for Terrestrial Broadcast and Cable (Revision B).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAtscContentAdvisoryDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAtscContentAdvisoryDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAtscContentAdvisoryDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/954d7dc4-43dd-4e33-a3cf-7584092cd0e7">GetLength</a>
</td>
<td align="left" width="63%">
Returns the length of the descriptor body.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9571bdb-5b0b-4798-b4dc-37ccee51a8b3">GetRatingRegionCount</a>
</td>
<td align="left" width="63%">
Returns the number of rating regions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f0a8073-0361-4320-a5d9-7c536a07e9c3">GetRecordRatedDimensions</a>
</td>
<td align="left" width="63%">
Returns the number of rating dimensions for a specified rating region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8a94a7ee-1909-4853-a72b-1174ee3c7803">GetRecordRatingDescriptionText</a>
</td>
<td align="left" width="63%">
Returns the rating description for a specified rating region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/583c9d8b-6b4b-4aa0-995d-26295b430f76">GetRecordRatingDimension</a>
</td>
<td align="left" width="63%">
Returns the dimension index into the rating region table (RRT) for a specified region.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb828399-d4aa-4e35-bb77-16795a598b35">GetRecordRatingRegion</a>
</td>
<td align="left" width="63%">
Returns the rating region at a specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c380d920-8d12-4965-8a5c-88e2f5861a09">GetRecordRatingValue</a>
</td>
<td align="left" width="63%">
Returns the rating value of a specified rating dimension.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd4c477f-54b1-4ebf-99e5-f75087d7599e">GetTag</a>
</td>
<td align="left" width="63%">
Returns the descriptor tag.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="https://msdn.microsoft.com/b88a6728-d772-48b8-aebc-7d4cc133320a">IAtscPsipParser::GetEIT</a> to get the <a href="https://msdn.microsoft.com/ab3fd79f-4ca6-418e-8e7c-a5fa196c09e6">IATSC_EIT</a> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/fdd7f03f-8e03-436f-bfe2-bb46a6a4b415">IATSC_EIT::GetRecordDescriptorByTag</a> and pass in the content advisory descriptor tag (0x87). If the descriptor is present, the method returns an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>IAtscContentAdvisoryDescriptor</b> interface.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

