---
UID: NN:vds.IVdsVdProvider
title: IVdsVdProvider
author: windows-sdk-content
description: Defines methods for creating and managing virtual disks.
old-location: base\ivdsvdprovider.htm
old-project: VDS
ms.assetid: 812e8ac5-91c5-455a-94e7-2edf55d92cdc
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: IVdsVdProvider, IVdsVdProvider interface, IVdsVdProvider interface,described, base.ivdsvdprovider, vds/IVdsVdProvider
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
 - IVdsVdProvider
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVdsVdProvider interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines methods for creating and managing virtual disks.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVdProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsVdProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVdProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef154bf3-ad30-4e6e-8292-af2037eced02">AddVDisk</a>
</td>
<td align="left" width="63%">
Creates a virtual disk object  for an existing virtual disk file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3655946d-f8b5-46a1-97e3-82b0831124b3">CreateVDisk</a>
</td>
<td align="left" width="63%">
Creates a virtual disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e0f1e7ef-fd72-48f5-895d-feabde4a3ded">GetDiskFromVDisk</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a> interface pointer for a virtual disk given an <a href="https://msdn.microsoft.com/2b4f81f9-81ec-4288-a26c-8ed4d378358a">IVdsVDisk</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ef5fd5e0-d11f-44e1-8947-787f1e592c5c">GetVDiskFromDisk</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/2b4f81f9-81ec-4288-a26c-8ed4d378358a">IVdsVDisk</a> interface pointer for the virtual disk given an <a href="https://msdn.microsoft.com/0fd6d1d4-daa6-4be3-8749-be98cd7c0288">IVdsDisk</a> interface pointer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/eab65da4-eb26-46f5-9978-972fd8dffb41">QueryVDisks</a>
</td>
<td align="left" width="63%">
Returns a list of all virtual disks that are managed by the provider.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2b4f81f9-81ec-4288-a26c-8ed4d378358a">IVdsVDisk</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

