---
UID: NN:vds.IVdsPack2
title: IVdsPack2
author: windows-sdk-content
description: Provides a method to create aligned volumes on a pack.
old-location: base\ivdspack2.htm
old-project: VDS
ms.assetid: b0124293-693d-412a-a97f-d0dae05a3bfc
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsPack2, IVdsPack2 interface, IVdsPack2 interface,described, base.ivdspack2, vds/IVdsPack2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: vds.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
-	IVdsPack2
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsPack2 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method to create aligned volumes on a pack.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsPack2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsPack2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsPack2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc7de88b-af6c-4d39-9297-49e33810466a">CreateVolume2</a>
</td>
<td align="left" width="63%">
Creates a volume in a disk pack with an optional alignment parameter.

</td>
</tr>
</table> 

