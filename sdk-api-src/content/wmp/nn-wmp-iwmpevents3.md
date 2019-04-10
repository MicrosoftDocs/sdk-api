---
UID: NN:wmp.IWMPEvents3
title: IWMPEvents3 (wmp.h)
author: windows-sdk-content
description: The IWMPEvents3 interface provides access to events originating from the Windows Media Player 11 control so that an application that has this control embedded in it can respond to these events.
old-location: wmp\iwmpevents3.htm
tech.root: WMP
ms.assetid: 654b7d78-97d4-4770-9729-dd1fed0431d9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPEvents3, IWMPEvents3 interface [Windows Media Player], IWMPEvents3 interface [Windows Media Player],described, IWMPEvents3Interface, wmp.iwmpevents3, wmp/IWMPEvents3
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
 - IWMPEvents3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents3 interface


## -description



The <b>IWMPEvents3</b> interface provides access to events originating from the Windows Media Player 11 control so that an application that has this control embedded in it can respond to these events. The events exposed by <b>IWMPEvents3</b> are also exposed by the <a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents</a> interface.



The events provided by <b>IWMPEvents3</b> extend the set of events provided by <a href="https://msdn.microsoft.com/en-us/library/Dd563310(v=VS.85).aspx">IWMPEvents</a> and <a href="https://msdn.microsoft.com/en-us/library/Dd563289(v=VS.85).aspx">IWMPEvents2</a> by adding events related to CD ripping, CD burning, folder monitoring, and remote library services.

In addition to the methods inherited from <a href="https://msdn.microsoft.com/en-us/library/Dd563289(v=VS.85).aspx">IWMPEvents2</a>, the <b>IWMPEvents3</b> interface exposes the following methods.
<table>
<tr>
<th>Method
          </th>
<th>Description
          </th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563297(v=VS.85).aspx">CdromBurnError</a>
</td>
<td>Occurs when a generic error happens during a CD burning operation.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563298(v=VS.85).aspx">CdromBurnMediaError</a>
</td>
<td>Occurs when an error happens while burning an individual media item to a CD.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563299(v=VS.85).aspx">CdromBurnStateChange</a>
</td>
<td>Occurs when a CD burning operation changes state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563300(v=VS.85).aspx">CdromRipMediaError</a>
</td>
<td>Occurs when an error happens while ripping an individual track from a CD.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563301(v=VS.85).aspx">CdromRipStateChange</a>
</td>
<td>Occurs when a CD ripping operation changes state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563302(v=VS.85).aspx">FolderScanStateChange</a>
</td>
<td>Occurs when a folder monitoring operation changes state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563303(v=VS.85).aspx">LibraryConnect</a>
</td>
<td>Occurs when a library becomes available.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563304(v=VS.85).aspx">LibraryDisconnect</a>
</td>
<td>Occurs when a library is no longer available.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563305(v=VS.85).aspx">MediaCollectionMediaAdded</a>
</td>
<td>Occurs when a media item is added to the local library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563306(v=VS.85).aspx">MediaCollectionMediaRemoved</a>
</td>
<td>Occurs when a media item is removed from the local library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563307(v=VS.85).aspx">StringCollectionChange</a>
</td>
<td>Occurs when a string collection changes.</td>
</tr>
</table> 
<ul>
<li>
<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5d9eb1c7-7022-4442-b67a-6a96fe5ce97f">Handling Events in C++</a>
</li>
<li>
<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd563310(v=VS.85).aspx">IWMPEvents Interface</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Dd563289(v=VS.85).aspx">IWMPEvents2 Interface</a>
</li>
</ul><table>
<tr>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563295(v=VS.85).aspx">Previous</a>
</td>
<td></td>
<td>
<a href="https://msdn.microsoft.com/en-us/library/Dd563297(v=VS.85).aspx">Next</a>
</td>
</tr>
</table> 

