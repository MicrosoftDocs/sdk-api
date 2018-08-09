---
UID: NN:mswmdm.IWMDMStorageControl
title: IWMDMStorageControl
author: windows-sdk-content
description: The IWMDMStorageControl interface is used to insert, delete, or move files within a storage, a device, or between a device and the computer.
old-location: wmdm\iwmdmstoragecontrol.htm
old-project: WMDM
ms.assetid: b56edc7a-0764-449a-95b4-da759e99fadd
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMDMStorageControl, IWMDMStorageControl interface [windows Media Device Manager], IWMDMStorageControl interface [windows Media Device Manager],described, IWMDMStorageControlInterface, mswmdm/IWMDMStorageControl, wmdm.iwmdmstoragecontrol
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
 - IWMDMStorageControl
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorageControl interface


## -description



The <b>IWMDMStorageControl</b> interface is used to insert, delete, or move files within a storage, a device, or between a device and the computer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorageControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDMStorageControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDMStorageControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2b044d2-6386-4c2e-a437-5ebddf827fb4">Delete</a>
</td>
<td align="left" width="63%">
Permanently deletes this storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/909b94fd-99de-4e26-87d6-d074a6eb5da3">Insert</a>
</td>
<td align="left" width="63%">
Puts content into the storage on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a2cfca0-66e6-4358-99c1-161f7baccdd5">Move</a>
</td>
<td align="left" width="63%">
Moves the storage to a new location on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a>
</td>
<td align="left" width="63%">
Copies the current storage to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/06cd302b-7876-4256-aa75-27127eb45ac9">Rename</a>
</td>
<td align="left" width="63%">
Renames the current storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c5a17642-5253-4d01-895a-09d00284f341">IWMDMStorageControl2 Interface</a>



<a href="https://msdn.microsoft.com/bc5165c2-791d-4549-a271-78728625b219">IWMDMStorageControl3 Interface</a>



<a href="https://msdn.microsoft.com/bea867d6-a875-4150-9958-7f683cd215b9">Interfaces for Applications</a>
 

 

