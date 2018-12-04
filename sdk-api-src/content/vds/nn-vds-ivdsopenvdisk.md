---
UID: NN:vds.IVdsOpenVDisk
title: IVdsOpenVDisk
author: windows-sdk-content
description: Defines methods for managing a virtual disk.
old-location: base\ivdsopenvdisk.htm
tech.root: vds
ms.assetid: 3d5f080f-3e83-437e-8cbc-9730988f5dcc
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVdsOpenVDisk, IVdsOpenVDisk interface, IVdsOpenVDisk interface,described, base.ivdsopenvdisk, vds/IVdsOpenVDisk
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
 - IVdsOpenVDisk
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVdsOpenVDisk interface


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Defines methods for managing a virtual disk.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVdsOpenVDisk</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVdsOpenVDisk</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVdsOpenVDisk</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/02647fe6-b94c-43ac-939c-262cea2c49d4">Attach</a>
</td>
<td align="left" width="63%">
Attaches a virtual disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/011adaae-3a17-4643-ae8d-400753019c83">Compact</a>
</td>
<td align="left" width="63%">
Compacts the virtual disk to reduce the physical size of the backing file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b720f6fc-f6a0-4cda-b710-30941bb79a06">Detach</a>
</td>
<td align="left" width="63%">
Detaches a virtual disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/79179da4-3c88-480b-bfb8-c4315fa56c4e">DetachAndDelete</a>
</td>
<td align="left" width="63%">
Detaches a virtual disk and deletes the backing files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6ba166de-8045-4ccb-8771-fc4dd9438c1f">Expand</a>
</td>
<td align="left" width="63%">
Increases the size of a virtual disk to the maximum size available on a fixed or expandable disk.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b513e904-a6ff-494e-9f63-b5158467b245">Merge</a>
</td>
<td align="left" width="63%">
Merges a child virtual disk with its parents in the differencing chain.

</td>
</tr>
</table> 

