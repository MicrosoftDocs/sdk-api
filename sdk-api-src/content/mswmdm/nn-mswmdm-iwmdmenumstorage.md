---
UID: NN:mswmdm.IWMDMEnumStorage
title: IWMDMEnumStorage
author: windows-sdk-content
description: The IWMDMEnumStorage interface enumerates storages on a device.
old-location: wmdm\iwmdmenumstorage.htm
old-project: WMDM
ms.assetid: 6ea80ab2-718b-464e-a805-9910460931bb
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IWMDMEnumStorage, IWMDMEnumStorage interface [windows Media Device Manager], IWMDMEnumStorage interface [windows Media Device Manager],described, IWMDMEnumStorageInterface, mswmdm/IWMDMEnumStorage, wmdm.iwmdmenumstorage
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
 - IWMDMEnumStorage
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMEnumStorage interface


## -description



The <b>IWMDMEnumStorage</b> interface enumerates storages on a device. Obtain this interface the first time by calling <a href="https://msdn.microsoft.com/ffd3c51a-7ec2-4ce5-9260-2b08bfa88a99">IWMDMDevice::EnumStorage</a> on a device, and afterward by calling <a href="https://msdn.microsoft.com/ab3c6a17-5a86-419b-b528-fd0db718de8f">IWMDMStorage::EnumStorage</a>. This interface only enumerates the immediate children of the parent storage that was used to obtain this interface. (If IWMDMDevice::EnumStorage was used, the parent storage is the device's root storage.)




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMEnumStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMEnumStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMEnumStorage</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938510">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator with the same enumeration state as the current enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the next sibling storage

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Sets the enumeration sequence back to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of storage devices or separate items of content in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/8b171b8a-00b7-4873-a4f7-1a0f29ad5cc0">Exploring a Device</a>



<a href="https://msdn.microsoft.com/ab3c6a17-5a86-419b-b528-fd0db718de8f">IWMDMStorage::EnumStorage</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

