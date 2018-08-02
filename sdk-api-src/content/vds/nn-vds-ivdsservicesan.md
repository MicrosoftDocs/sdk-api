---
UID: NN:vds.IVdsServiceSAN
title: IVdsServiceSAN
author: windows-sdk-content
description: Provides methods for managing disk online and offline SAN policy for the operating system.
old-location: base\ivdsservicesan.htm
old-project: VDS
ms.assetid: 675e9ea8-06b6-4832-9311-17361e4781d4
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVdsServiceSAN, IVdsServiceSAN interface, IVdsServiceSAN interface,described, base.ivdsservicesan, vds/IVdsServiceSAN
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVdsServiceSAN
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsServiceSAN interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods for managing disk online and offline <a href="https://msdn.microsoft.com/2da99388-8ee6-4e6b-98dc-52f12290c4dc">SAN policy</a> for the operating system.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsServiceSAN</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsServiceSAN</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsServiceSAN</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59602d97-2fdf-4d1b-b158-e545619397e0">GetSANPolicy</a>
</td>
<td align="left" width="63%">
Gets the disk SAN policy for the operating system.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5cb0b5e-d181-44a7-8416-e9f8fb575423">SetSANPolicy</a>
</td>
<td align="left" width="63%">
Sets the disk SAN policy for the operating system.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2da99388-8ee6-4e6b-98dc-52f12290c4dc">VDS_SAN_POLICY</a>
 

 

