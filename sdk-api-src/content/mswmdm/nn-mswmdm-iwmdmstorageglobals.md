---
UID: NN:mswmdm.IWMDMStorageGlobals
title: IWMDMStorageGlobals
author: windows-sdk-content
description: The IWMDMStorageGlobals interface provides methods for retrieving global information about a storage medium (such as a flash ROM card) on a device.
old-location: wmdm\iwmdmstorageglobals.htm
old-project: WMDM
ms.assetid: fe164271-58f0-4b28-a200-6b15f8b42d36
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IWMDMStorageGlobals, IWMDMStorageGlobals interface [windows Media Device Manager], IWMDMStorageGlobals interface [windows Media Device Manager],described, IWMDMStorageGlobalsInterface, mswmdm/IWMDMStorageGlobals, wmdm.iwmdmstorageglobals
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mswmdm.h
api_name:
 - IWMDMStorageGlobals
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorageGlobals interface


## -description



The <b>IWMDMStorageGlobals</b> interface provides methods for retrieving global information about a storage <i>medium</i> (such as a flash ROM card) on a device. This can include the amount of free space, the total number of files, and so on. The values returned by this interface apply to the root storage of the current storage. Note that this is not necessarily equivalent to a device, since a device may have more than one storage (each flash card is considered a separate storage, for instance).

This interface is acquired by calling <b>IWMDMStorage::GetStorageGlobals</b>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorageGlobals</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMStorageGlobals</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorageGlobals</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451391">GetCapabilities</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/13783d0e-82e6-4340-bb06-85b8d3d06b5c">GetSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves a serial number that uniquely identifies the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406321">GetStatus</a>
</td>
<td align="left" width="63%">
Retrieves the current status of the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/40e1a39b-2757-472c-b585-77b829605e8c">GetTotalBad</a>
</td>
<td align="left" width="63%">
Retrieves the total amount of unusable space on the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a97c2d92-dc54-4987-b2b4-e4de2e546a1f">GetTotalFree</a>
</td>
<td align="left" width="63%">
Retrieves the total free space on the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebbc8b7e-037f-4b8d-b026-793d38914685">GetTotalSize</a>
</td>
<td align="left" width="63%">
Retrieves the total size of the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Formats the storage medium.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

