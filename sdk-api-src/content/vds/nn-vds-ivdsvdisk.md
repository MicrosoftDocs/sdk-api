---
UID: NN:vds.IVdsVDisk
title: IVdsVDisk
author: windows-sdk-content
description: Defines methods for managing a virtual disk.
old-location: base\ivdsvdisk.htm
tech.root: vds
ms.assetid: 2b4f81f9-81ec-4288-a26c-8ed4d378358a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IVdsVDisk, IVdsVDisk interface, IVdsVDisk interface,described, base.ivdsvdisk, vds/IVdsVDisk
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
 - IVdsVDisk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsVDisk interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines methods for managing a virtual disk.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsVDisk</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsVDisk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsVDisk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ce60f7f-a7f2-4e1e-aae0-bd082b62480f">GetDeviceName</a>
</td>
<td align="left" width="63%">
Returns the device name for the volume where the virtual disk resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e8ab5d3a-775d-4c80-9c18-d25b5dd169e6">GetHostVolume</a>
</td>
<td align="left" width="63%">
Returns an interface pointer to the volume object for the volume where the virtual disk resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ecfbd1f-2f67-4d79-b081-7df071b070a4">GetProperties</a>
</td>
<td align="left" width="63%">
Returns disk property information for the volume where the virtual disk resides.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e633f934-8f2d-4614-b34c-87bb74ebf385">Open</a>
</td>
<td align="left" width="63%">
Opens a handle to the specified virtual disk file and returns an <a href="https://msdn.microsoft.com/3d5f080f-3e83-437e-8cbc-9730988f5dcc">IVdsOpenVDisk</a> interface pointer to the object that represents the opened handle.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/812e8ac5-91c5-455a-94e7-2edf55d92cdc">IVdsVdProvider</a>



<a href="https://msdn.microsoft.com/0bddfd62-881d-4fda-b303-ed38d434af55">VDS Interfaces</a>
 

 

