---
UID: NN:vds.IVdsDiskOnline
title: IVdsDiskOnline
author: windows-sdk-content
description: Provides methods to bring a disk online and take it offline.Windows Vista:  This interface is not supported until Windows Vista with Service Pack 1 (SP1). Use IVdsDisk2 instead.
old-location: base\ivdsdiskonline.htm
tech.root: VDS
ms.assetid: f30ceaa0-ff4b-49fb-b140-b6725810cd06
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IVdsDiskOnline, IVdsDiskOnline interface, IVdsDiskOnline interface,described, base.ivdsdiskonline, vds/IVdsDiskOnline
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVdsDiskOnline
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsDiskOnline interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides methods to bring a disk online and take it offline.<b>Windows Vista:  </b>This interface is not supported until Windows Vista with Service Pack 1 (SP1). Use <a href="https://msdn.microsoft.com/9fb8a08e-412d-415a-aa27-cc0180599903">IVdsDisk2</a> instead.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDiskOnline</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsDiskOnline</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDiskOnline</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f27dd46-2fa1-4522-9d35-db78255c6d11">Offline</a>
</td>
<td align="left" width="63%">
Takes the disk offline.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3366bc7-18ca-4a90-b4e7-e6213a7cc002">Online</a>
</td>
<td align="left" width="63%">
Brings the disk online.

</td>
</tr>
</table> 

