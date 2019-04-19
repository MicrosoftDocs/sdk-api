---
UID: NN:wmp.IWMPFolderMonitorServices
title: IWMPFolderMonitorServices (wmp.h)
author: windows-sdk-content
description: The IWMPFolderMonitorServices interface is deprecated.The IWMPFolderMonitorServices interface provides methods to enumerate, scan, and modify file folders that Windows Media Player monitors for digital media content.To use this interface, you must create a remoted instance of the Windows Media Player 11 control. For more information about remoting, see Remoting the Windows Media Player Control.
old-location: wmp\iwmpfoldermonitorservices.htm
tech.root: WMP
ms.assetid: 42c3b03c-f8f8-4219-91e1-da54a175fb24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPFolderMonitorServices, IWMPFolderMonitorServices interface [Windows Media Player], IWMPFolderMonitorServices interface [Windows Media Player],described, IWMPFolderMonitorServicesInterface, wmp.iwmpfoldermonitorservices, wmp/IWMPFolderMonitorServices
ms.topic: interface
req.header: wmp.h
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
 - wmp.h
api_name:
 - IWMPFolderMonitorServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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
<a href="https://msdn.microsoft.com/en-us/library/Dd563367(v=VS.85).aspx">add</a>
</td>
<td align="left" width="63%">
Adds a folder to the list of monitored folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563369(v=VS.85).aspx">get_addedFilesCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of files added to the library during the current scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563370(v=VS.85).aspx">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the count of monitored folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563371(v=VS.85).aspx">get_currentFolder</a>
</td>
<td align="left" width="63%">
Retrieves the path of the folder currently being scanned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563372(v=VS.85).aspx">get_scannedFilesCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of files inspected during the current scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563373(v=VS.85).aspx">get_scanState</a>
</td>
<td align="left" width="63%">
Retrieves the scan state for the current scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563374(v=VS.85).aspx">get_updateProgress</a>
</td>
<td align="left" width="63%">
Retrieves the update progress as percent complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563375(v=VS.85).aspx">item</a>
</td>
<td align="left" width="63%">
Retrieves the path of the folder corresponding to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563376(v=VS.85).aspx">remove</a>
</td>
<td align="left" width="63%">
Removes a folder from the list of monitored folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563377(v=VS.85).aspx">startScan</a>
</td>
<td align="left" width="63%">
Starts a scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563378(v=VS.85).aspx">stopScan</a>
</td>
<td align="left" width="63%">
Stops the scanning operation.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPFolderMonitorServices</b> by calling <b>QueryInterface</b> through <a href="https://msdn.microsoft.com/en-us/library/Dd563514(v=VS.85).aspx">IWMPPlayer</a>.
	


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563514(v=VS.85).aspx">IWMPPlayer Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
 

 

