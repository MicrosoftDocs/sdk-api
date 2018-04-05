---
UID: NN:mswmdm.IMDSPStorageGlobals
title: IMDSPStorageGlobals
author: windows-driver-content
description: The IMDSPStorageGlobals interface, acquired from the IMDSPStorage interface, provides methods for retrieving global information about a storage medium. This might include the amount of free space, serial number of the medium, and so on.
old-location: wmdm\imdspstorageglobals.htm
old-project: WMDM
ms.assetid: 70653352-a467-4197-93e3-e8fb45f99d34
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IMDSPStorageGlobals, IMDSPStorageGlobals interface [windows Media Device Manager], IMDSPStorageGlobals interface [windows Media Device Manager], described, IMDSPStorageGlobalsInterface, mswmdm/IMDSPStorageGlobals, wmdm.imdspstorageglobals
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: MSVidCtlStateList
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mswmdm.h
api_name:
-	IMDSPStorageGlobals
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMDSPStorageGlobals interface


## -description



The <b>IMDSPStorageGlobals</b> interface, acquired from the <a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage</a> interface, provides methods for retrieving global information about a storage medium. This might include the amount of free space, serial number of the medium, and so on.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMDSPStorageGlobals</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMDSPStorageGlobals</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMDSPStorageGlobals</b> interface has these methods.
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
Retrieves the capabilities of the storage medium that an instance of this interface is associated with.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451305">GetDevice</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the device with which this interface is associated.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80b6cb71-d567-4fb5-9f75-82ae2fe118c7">GetRootStorage</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the <b>IMDSPStorage</b> interface for the root storage of the storage medium.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/42765429-c230-4fa1-9e2e-e21c71e49ae0">GetSerialNumber</a>
</td>
<td align="left" width="63%">
Retrieves a serial number uniquely identifying the storage medium.

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
<a href="https://msdn.microsoft.com/b0cbf636-e2c4-4a30-9b6d-5833090330a4">GetTotalBad</a>
</td>
<td align="left" width="63%">
Retrieves the total amount of unusable space on the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/141b33e8-5cb5-46a8-b91e-01bd9c634cbf">GetTotalFree</a>
</td>
<td align="left" width="63%">
Retrieves the total free space on the storage medium, in bytes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a4b4ac5-0b7e-4a22-9857-b251a6bf1dcf">GetTotalSize</a>
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




<a href="https://msdn.microsoft.com/f22b8a6d-7df8-4fea-9436-79b9ded25a40">IMDSPStorage Interface</a>



<a href="https://msdn.microsoft.com/bd61c5fa-047c-4d93-bae1-f3433696b95b">Interfaces for Service Providers</a>
 

 

