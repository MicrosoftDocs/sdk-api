---
UID: NN:vdshwprv.IVdsProvider
title: IVdsProvider
author: windows-sdk-content
description: Returns the properties of a hardware or software provider.
old-location: base\ivdsprovider.htm
tech.root: vds
ms.assetid: c09aa32f-d859-44b1-8656-973ba1b6a167
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsProvider, IVdsProvider interface [VDS], IVdsProvider interface [VDS],described, base.ivdsprovider, vds/IVdsProvider, vdshwprv/IVdsProvider
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsProvider interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Returns the properties of 
   a hardware or software provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4cb18c5-2cda-4d0a-9be0-4a548ec2f6eb">GetProperties</a>
</td>
<td align="left" width="63%">
Returns the properties of the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b6e7ca7c-b95f-457d-996b-b3c449b6ce6b">IVdsPack::GetProvider</a>



<a href="https://msdn.microsoft.com/55171eb1-6fec-4651-914c-88d23e8d7849">IVdsService::QueryProviders</a>



<a href="https://msdn.microsoft.com/317e4aa3-2635-4e1b-af2d-ad7c6170bf33">IVdsSubSystem::GetProvider</a>



<a href="https://msdn.microsoft.com/131e927d-d32a-44f6-8aae-28839cfa9e7d">Provider Object</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>



<a href="https://msdn.microsoft.com/f41fc908-3720-4dfb-a5d3-bb1459fb7e5d">VDS_PROVIDER_PROP</a>
 

 

