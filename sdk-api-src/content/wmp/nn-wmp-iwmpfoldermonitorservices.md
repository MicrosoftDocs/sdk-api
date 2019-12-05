---
UID: NN:wmp.IWMPFolderMonitorServices
title: IWMPFolderMonitorServices (wmp.h)
description: The IWMPFolderMonitorServices interface is deprecated.The IWMPFolderMonitorServices interface provides methods to enumerate, scan, and modify file folders that Windows Media Player monitors for digital media content.To use this interface, you must create a remoted instance of the Windows Media Player 11 control. For more information about remoting, see Remoting the Windows Media Player Control.
old-location: wmp\iwmpfoldermonitorservices.htm
tech.root: WMP
ms.assetid: 42c3b03c-f8f8-4219-91e1-da54a175fb24
ms.date: 12/05/2018
ms.keywords: IWMPFolderMonitorServices, IWMPFolderMonitorServices interface [Windows Media Player], IWMPFolderMonitorServices interface [Windows Media Player],described, IWMPFolderMonitorServicesInterface, wmp.iwmpfoldermonitorservices, wmp/IWMPFolderMonitorServices
ms.topic: interface
f1_keywords:
- wmp/IWMPFolderMonitorServices
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPFolderMonitorServices interface


## -description



The <b>IWMPFolderMonitorServices</b> interface is deprecated.

The <b>IWMPFolderMonitorServices</b> interface provides methods to enumerate, scan, and modify file folders that Windows Media Player monitors for digital media content.

To use this interface, you must create a remoted instance of the Windows Media Player 11 control. For more information about remoting, see <a href="https://docs.microsoft.com/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPFolderMonitorServices</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPFolderMonitorServices</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-add">add</a>
</td>
<td align="left" width="63%">
Adds a folder to the list of monitored folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_addedfilescount">get_addedFilesCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of files added to the library during the current scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_count">get_count</a>
</td>
<td align="left" width="63%">
Retrieves the count of monitored folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_currentfolder">get_currentFolder</a>
</td>
<td align="left" width="63%">
Retrieves the path of the folder currently being scanned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scannedfilescount">get_scannedFilesCount</a>
</td>
<td align="left" width="63%">
Retrieves the count of files inspected during the current scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_scanstate">get_scanState</a>
</td>
<td align="left" width="63%">
Retrieves the scan state for the current scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-get_updateprogress">get_updateProgress</a>
</td>
<td align="left" width="63%">
Retrieves the update progress as percent complete.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-item">item</a>
</td>
<td align="left" width="63%">
Retrieves the path of the folder corresponding to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-remove">remove</a>
</td>
<td align="left" width="63%">
Removes a folder from the list of monitored folders.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-startscan">startScan</a>
</td>
<td align="left" width="63%">
Starts a scanning operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpfoldermonitorservices-stopscan">stopScan</a>
</td>
<td align="left" width="63%">
Stops the scanning operation.

</td>
</tr>
</table> 

Retrieve a pointer to <b>IWMPFolderMonitorServices</b> by calling <b>QueryInterface</b> through <a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer</a>.
	


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplayer">IWMPPlayer Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>
 

 

