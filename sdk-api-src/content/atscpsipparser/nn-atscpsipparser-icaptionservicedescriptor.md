---
UID: NN:atscpsipparser.ICaptionServiceDescriptor
title: ICaptionServiceDescriptor
author: windows-sdk-content
description: This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
old-location: mstv\icaptionservicedescriptor.htm
old-project: mstv
ms.assetid: fc1f38af-2fe8-4c08-b6f8-312dd4771141
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ICaptionServiceDescriptor, ICaptionServiceDescriptor interface [Microsoft TV Technologies], ICaptionServiceDescriptor interface [Microsoft TV Technologies],described, ICaptionServiceDescriptorInterface, atscpsipparser/ICaptionServiceDescriptor, mstv.icaptionservicedescriptor
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
req.typenames: AsyncStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	atscpsipparser.h
api_name:
-	ICaptionServiceDescriptor
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICaptionServiceDescriptor interface


## -description



This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        

The <b>ICaptionServiceDescriptor</b> interface enables the client to get caption service descriptors from a Program and System Information Protocol (PSIP) table in an ATSC stream. The content advisor descriptor may be present in the event information table (EIT). For more information, refer to ATSC Standard A/65B, Program and System Information Protocol for Terrestrial Broadcast and Cable (Revision B).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICaptionServiceDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICaptionServiceDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICaptionServiceDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e8ca631-45fd-462c-bab9-4a242751f212">GetCaptionServiceNumber</a>
</td>
<td align="left" width="63%">
Returns the Service Number for a specified caption service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d245118a-3ff2-4ea7-9ff9-f8c1991f2073">GetCCType</a>
</td>
<td align="left" width="63%">
Queries whether a caption service contains Digital Television Closed Captioning (DTVCC) or line-21 closed captioning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ecf31c8-b93e-4c6c-991c-33ce942757ec">GetEasyReader</a>
</td>
<td align="left" width="63%">
Queries whether a caption service contains "Easy Reader" captions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b3b31dd-83cc-4067-a46f-929e1a75087a">GetLanguageCode</a>
</td>
<td align="left" width="63%">
Returns the language code for a specified caption service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50c2baff-a355-45a4-8a05-a193e695c448">GetNumberOfServices</a>
</td>
<td align="left" width="63%">
Returns the number of caption services.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/921d919a-5e23-4c09-abff-3ed1e7dbec01">GetWideAspectRatio</a>
</td>
<td align="left" width="63%">
Queries whether a caption service is formatted for wide-screen displays.

</td>
</tr>
</table> 


## -remarks



To obtain a pointer to this interface, do the following:

<ol>
<li>Call <a href="https://msdn.microsoft.com/b88a6728-d772-48b8-aebc-7d4cc133320a">IAtscPsipParser::GetEIT</a> to get the <a href="https://msdn.microsoft.com/ab3fd79f-4ca6-418e-8e7c-a5fa196c09e6">IATSC_EIT</a> interface.</li>
<li>Call <a href="https://msdn.microsoft.com/fdd7f03f-8e03-436f-bfe2-bb46a6a4b415">IATSC_EIT::GetRecordDescriptorByTag</a> and pass in the caption service descriptor tag (0x86). If the descriptor is present, the method returns an <a href="https://msdn.microsoft.com/efca0ecf-eb3e-4dcd-a674-b8fe1a66ff84">IGenericDescriptor</a> pointer.</li>
<li>Query the returned <b>IGenericDescriptor</b> pointer for the <b>ICaptionServiceDescriptor</b> interface.</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

