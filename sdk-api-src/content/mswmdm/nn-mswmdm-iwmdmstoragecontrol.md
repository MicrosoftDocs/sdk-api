---
UID: NN:mswmdm.IWMDMStorageControl
title: IWMDMStorageControl (mswmdm.h)
description: The IWMDMStorageControl interface is used to insert, delete, or move files within a storage, a device, or between a device and the computer.
old-location: wmdm\iwmdmstoragecontrol.htm
tech.root: WMDM
ms.assetid: b56edc7a-0764-449a-95b4-da759e99fadd
ms.date: 12/05/2018
ms.keywords: IWMDMStorageControl, IWMDMStorageControl interface [windows Media Device Manager], IWMDMStorageControl interface [windows Media Device Manager],described, IWMDMStorageControlInterface, mswmdm/IWMDMStorageControl, wmdm.iwmdmstoragecontrol
ms.topic: interface
f1_keywords:
- mswmdm/IWMDMStorageControl
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mswmdm.h
api_name:
- IWMDMStorageControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDMStorageControl interface


## -description



The <b>IWMDMStorageControl</b> interface is used to insert, delete, or move files within a storage, a device, or between a device and the computer.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDMStorageControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDMStorageControl</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-delete">Delete</a>
</td>
<td align="left" width="63%">
Permanently deletes this storage.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert">Insert</a>
</td>
<td align="left" width="63%">
Puts content into the storage on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-move">Move</a>
</td>
<td align="left" width="63%">
Moves the storage to a new location on the device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read">Read</a>
</td>
<td align="left" width="63%">
Copies the current storage to the computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-rename">Rename</a>
</td>
<td align="left" width="63%">
Renames the current storage.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol2">IWMDMStorageControl2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol3">IWMDMStorageControl3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMDM/interfaces-for-applications">Interfaces for Applications</a>
 

 

