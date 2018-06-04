---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IWMPFolderMonitorServices interface


## -description



The <b>IWMPFolderMonitorServices</b> interface is deprecated.

The <b>IWMPFolderMonitorServices</b> interface provides methods to enumerate, scan, and modify file folders that Windows Media Player monitors for digital media content.

To use this interface, you must create a remoted instance of the Windows Media Player 11 control. For more information about remoting, see <a href="https://msdn.microsoft.com/d543b2a0-a2cb-47e2-b50e-4513fc061b46">Remoting the Windows Media Player Control</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPFolderMonitorServices</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMPFolderMonitorServices</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPFolderMonitorServices</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">add</a>
</td>
<td align="left" width="63%">
Adds a folder to the list of monitored folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/56dcbb46-8de9-4fbe-b82c-927d42e39b2b">get_addedFilesCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of files added to the library during the current scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf80820a-d126-4af6-ba5e-c1188c5c00a4">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the count of monitored folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b0bc2f6a-c5ab-4dc5-a574-5b0fde16449a">get_currentFolder</a>
</td>
<td align="left" width="63%">
Retrieves the path of the folder currently being scanned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8b6a291b-b28d-4415-813c-5f4a5e1b2dca">get_scannedFilesCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of files inspected during the current scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f13d2d0-5d8c-4aa7-bc69-c5c0436337a6">get_scanState</a>
</td>
<td align="left" width="63%">
Retrieves the scan state for the current scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60a612d2-8675-456f-b428-ddfd0b73fd83">get_updateProgress</a>
</td>
<td align="left" width="63%">
Retrieves the update progress as percent complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">item</a>
</td>
<td align="left" width="63%">
Retrieves the path of the folder corresponding to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">remove</a>
</td>
<td align="left" width="63%">
Removes a folder from the list of monitored folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c54c5b7e-3abf-4006-a811-c80b06e6def9">startScan</a>
</td>
<td align="left" width="63%">
Starts a scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b85cefb-3118-4e7f-b6f7-2f387057895e">stopScan</a>
</td>
<td align="left" width="63%">
Stops the scanning operation.

</td>
</tr>
</table> 


Retrieve a pointer to <b>IWMPFolderMonitorServices</b> by calling <b>QueryInterface</b> through <a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer</a>.
	


## -see-also




<a href="https://msdn.microsoft.com/ce6aef79-1faa-44ac-a096-f65d09458067">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

