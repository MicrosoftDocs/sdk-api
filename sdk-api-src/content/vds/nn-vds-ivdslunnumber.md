---
UID: NN:vds.IVdsLunNumber
title: IVdsLunNumber
author: windows-sdk-content
description: Provides a method to query the LUN number for a LUN.
old-location: base\ivdslunnumber.htm
tech.root: vds
ms.assetid: 77bd95f7-005a-474f-97c4-e211432b447d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsLunNumber, IVdsLunNumber interface, IVdsLunNumber interface,described, base.ivdslunnumber, vds/IVdsLunNumber, vdshwprv/IVdsLunNumber
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IVdsLunNumber
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsLunNumber interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method to query the LUN number for a LUN.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsLunNumber</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsLunNumber</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsLunNumber</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79aa7dc1-ef46-4b6d-8088-e42839625a16">GetLunNumber</a>
</td>
<td align="left" width="63%">
Retrieves the LUN number for a LUN.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

