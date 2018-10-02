---
UID: NN:vds.IVdsDisk3
title: IVdsDisk3
author: windows-sdk-content
description: Provides a method to retrieve property information for a disk, including the disk's location path.
old-location: base\ivdsdisk3.htm
tech.root: VDS
ms.assetid: e3004195-b180-4053-bf91-8f1a0e72f5a6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IVdsDisk3, IVdsDisk3 interface, IVdsDisk3 interface,described, base.ivdsdisk3, vds/IVdsDisk3
ms.prod: windows
ms.technology: windows-sdk
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
 - IVdsDisk3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsDisk3 interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Provides a method to retrieve property information for a disk, including the disk's location path.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsDisk3</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsDisk3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsDisk3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef88b61b-9139-4767-b54f-46122650e922">GetProperties2</a>
</td>
<td align="left" width="63%">
Returns property 
   information for a disk. This method is identical to the <a href="https://msdn.microsoft.com/d2046a26-852d-46b2-b060-98b4a2a92387">IVdsDisk::GetProperties</a> method, except that it returns a <a href="https://msdn.microsoft.com/f51c2937-4b70-44fb-b626-1df072e2622a">VDS_DISK_PROP2</a> structure instead of a <a href="https://msdn.microsoft.com/c7c09f95-9489-46fd-8b03-cabdee4521cf">VDS_DISK_PROP</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ca2ebb6-1394-48a2-972b-bdf43bf58ced">QueryFreeExtents</a>
</td>
<td align="left" width="63%">
Returns the free extents on the disk and aligns them to the specified alignment size.

</td>
</tr>
</table> 

