---
UID: NN:vds.IVdsSubSystemInterconnect
title: IVdsSubSystemInterconnect
author: windows-driver-content
description: Provides a method to query the interconnect types that are supported by a subsystem.
old-location: base\ivdssubsysteminterconnect.htm
old-project: VDS
ms.assetid: d690827a-4608-4d02-a3bb-5cdb5073b0ad
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: IVdsSubSystemInterconnect, IVdsSubSystemInterconnect interface, IVdsSubSystemInterconnect interface,described, base.ivdssubsysteminterconnect, vds/IVdsSubSystemInterconnect, vdshwprv/IVdsSubSystemInterconnect
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: VDS_VOLUME_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uuid.lib
-	Uuid.dll
api_name:
-	IVdsSubSystemInterconnect
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsSubSystemInterconnect interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method to query the interconnect types that are supported by a subsystem.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsSubSystemInterconnect</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsSubSystemInterconnect</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsSubSystemInterconnect</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5e8e69b4-023d-49f7-a363-bae1ae9536ac">GetSupportedInterconnects</a>
</td>
<td align="left" width="63%">
Returns the interconnect types that the subsystem supports.

</td>
</tr>
</table> 

