---
UID: NN:vds.IVdsHbaPort
title: IVdsHbaPort
author: windows-sdk-content
description: Provides methods to query and interact with HBA ports on the local system.
old-location: base\ivdshbaport.htm
old-project: vds
ms.assetid: beb6ae5c-b70a-4dbc-b16f-1b398a569f15
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IVdsHbaPort, IVdsHbaPort interface [VDS], IVdsHbaPort interface [VDS],described, base.ivdshbaport, vds/IVdsHbaPort
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vds.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IVdsHbaPort
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsHbaPort interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to query and 
   interact with HBA ports on the local system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsHbaPort</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsHbaPort</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsHbaPort</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5472534f-66c8-4a78-a351-92f59e50ae32">GetProperties</a>
</td>
<td align="left" width="63%">
Retrieves the properties of an HBA port.</p> (Inherited from <b>IVdsHbaPort</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0df5b5f7-1fdc-41f1-96e4-2abe96c59228">SetAllPathStatuses</a>
</td>
<td align="left" width="63%">
Sets the statuses of all paths originating from the HBA port to a specified status.</p> (Inherited from <b>IVdsHbaPort</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

