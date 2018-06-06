---
UID: NN:mswmdm.IMDSPEnumStorage
title: IMDSPEnumStorage
author: windows-sdk-content
description: The IMDSPEnumStorage interface is used to enumerate the storage media on a device.
old-location: wmdm\imdspenumstorage.htm
old-project: WMDM
ms.assetid: fc2fed46-1f4d-4d53-a843-0f699b687a18
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: IMDSPEnumStorage, IMDSPEnumStorage interface [windows Media Device Manager], IMDSPEnumStorage interface [windows Media Device Manager],described, IMDSPEnumStorageInterface, mswmdm/IMDSPEnumStorage, wmdm.imdspenumstorage
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
 - IMDSPEnumStorage
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMDSPEnumStorage interface


## -description



The <b>IMDSPEnumStorage</b> interface is used to enumerate the storage media on a device. For more information on the standard implementation of enumeration interfaces, see the Microsoft COM documentation, available at the <a href="http://go.microsoft.com/fwlink/p/?linkid=3282">Microsoft Web site</a>. The storage media on a device are organized in a hierarchical manner similar to disk drives on a computer.

When accessed from the <a href="https://msdn.microsoft.com/bbf19979-8e09-476e-9401-443ab5e84866">IMDSPDevice::EnumStorage</a> method, this interface enumerates the individual storage media on the device in the same way that you would see the individual disk drives on a computer.

When accessed from the <a href="https://msdn.microsoft.com/ab3c6a17-5a86-419b-b528-fd0db718de8f">IWMDMStorage::EnumStorage</a> method, this interface enumerates the contents of the storage medium. <b>EnumStorage</b> can be called on the enumerated storage objects recursively, and thus the contents of a storage medium are returned in the hierarchical fashion in which they are stored on the storage medium. If the file system of the storage medium supports a notion of order among the content, the enumerator will return the contents in the same order.

The storage enumerator returns a snapshot of the state of storages. It may not reflect the effect of storage media insertion and removal and may not reflect the effects of subsequent <b>Insert</b>, <b>Move</b> and <b>Delete</b> methods. The client should obtain a new enumerator to get the new state of the storage media.

The <b>Insert</b>, <b>Move</b>, and <b>Delete</b> methods of the <a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl</a> interface change the order of files. If these operations are invoked, then the order of objects as originally returned by the <b>IMDSPEnumStorage</b> interface can be changed.

If an application is going to display the order of content on a media device, the application programmer must take into account order changes that can occur as a result of <b>IWMDMStorageControl</b> operations. There are two ways to deal with this situation. One way is to simply re-enumerate whenever a change to content occurs. Another way is to maintain the order of <b>IWMDMStorage</b> objects programmatically.

No matter how this issue is handled, it must be handled by the application if the order of files is important to the application.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPEnumStorage</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMDSPEnumStorage</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPEnumStorage</b> interface has these methods.
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
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the next <a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage</a> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926942">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of storage interface(s) in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/bbf19979-8e09-476e-9401-443ab5e84866">IMDSPDevice::EnumStorage</a>



<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage Interface</a>



<a href="https://msdn.microsoft.com/ab3c6a17-5a86-419b-b528-fd0db718de8f">IWMDMStorage::EnumStorage</a>



<a href="https://msdn.microsoft.com/b56edc7a-0764-449a-95b4-da759e99fadd">IWMDMStorageControl Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

