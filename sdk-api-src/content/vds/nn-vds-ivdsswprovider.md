---
UID: NN:vds.IVdsSwProvider
title: IVdsSwProvider
author: windows-sdk-content
description: Provides methods to perform operations specific to the software provider.
old-location: base\ivdsswprovider.htm
tech.root: vds
ms.assetid: 0602d4d6-a31d-4425-ad21-a267c6e1dd7b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsSwProvider, IVdsSwProvider interface [VDS], IVdsSwProvider interface [VDS],described, base.ivdsswprovider, vds/IVdsSwProvider
ms.topic: interface
req.header: vds.h
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
 - IVdsSwProvider
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsSwProvider interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to perform operations specific to the software provider.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSwProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsSwProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSwProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d711ed8-9101-4e68-b085-b5df01515b5d">CreatePack</a>
</td>
<td align="left" width="63%">
Creates a disk pack for the current software provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f30494d8-ae82-479d-a47a-7087129e7e6a">QueryPacks</a>
</td>
<td align="left" width="63%">
Returns an enumeration object that contains all packs managed by the software provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/131e927d-d32a-44f6-8aae-28839cfa9e7d">Provider Object</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

