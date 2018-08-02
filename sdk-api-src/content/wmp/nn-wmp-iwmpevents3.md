---
UID: NN:wmp.IWMPEvents3
title: IWMPEvents3
author: windows-sdk-content
description: The IWMPEvents3 interface provides access to events originating from the Windows Media Player 11 control so that an application that has this control embedded in it can respond to these events.
old-location: wmp\iwmpevents3.htm
old-project: WMP
ms.assetid: 654b7d78-97d4-4770-9729-dd1fed0431d9
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMPEvents3, IWMPEvents3 interface [Windows Media Player], IWMPEvents3 interface [Windows Media Player],described, IWMPEvents3Interface, wmp.iwmpevents3, wmp/IWMPEvents3
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WMPSyncState
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents3 interface


## -description



The <b>IWMPEvents3</b> interface provides access to events originating from the Windows Media Player 11 control so that an application that has this control embedded in it can respond to these events. The events exposed by <b>IWMPEvents3</b> are also exposed by the <a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents</a> interface.



The events provided by <b>IWMPEvents3</b> extend the set of events provided by <a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents</a> and <a href="https://msdn.microsoft.com/61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d">IWMPEvents2</a> by adding events related to CD ripping, CD burning, folder monitoring, and remote library services.

In addition to the methods inherited from <a href="https://msdn.microsoft.com/61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d">IWMPEvents2</a>, the <b>IWMPEvents3</b> interface exposes the following methods.
<table>
<tr>
<th>Method
          </th>
<th>Description
          </th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/ea1ded30-4fca-4208-9fc2-f93c169f33b6">CdromBurnError</a>
</td>
<td>Occurs when a generic error happens during a CD burning operation.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/4bad9de2-8899-4149-965c-7835bd854f6f">CdromBurnMediaError</a>
</td>
<td>Occurs when an error happens while burning an individual media item to a CD.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/8328f1bf-c928-4504-859f-f1b62e77e9e0">CdromBurnStateChange</a>
</td>
<td>Occurs when a CD burning operation changes state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/103f6d52-5b59-422d-918d-5004cbdfc75a">CdromRipMediaError</a>
</td>
<td>Occurs when an error happens while ripping an individual track from a CD.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/08445295-4fed-412f-84ce-eaf337758472">CdromRipStateChange</a>
</td>
<td>Occurs when a CD ripping operation changes state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/07e9a49b-19a6-4ed2-b037-fe44ada920a1">FolderScanStateChange</a>
</td>
<td>Occurs when a folder monitoring operation changes state.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/b9e1feb7-c894-4f37-9756-378740637f6e">LibraryConnect</a>
</td>
<td>Occurs when a library becomes available.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/eb0f4d9f-23b7-4fe7-b45d-152a2f64af30">LibraryDisconnect</a>
</td>
<td>Occurs when a library is no longer available.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/374ac1d8-ea7f-498a-b9b1-02bf7083f682">MediaCollectionMediaAdded</a>
</td>
<td>Occurs when a media item is added to the local library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/c142a5ab-deed-41d0-8ddd-1d2f8a7b9d69">MediaCollectionMediaRemoved</a>
</td>
<td>Occurs when a media item is removed from the local library.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/93880116-e354-49d0-ba02-391fbb4d3f8c">StringCollectionChange</a>
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
</li>
<li>
<a href="https://msdn.microsoft.com/396545d5-8844-4dd2-9ed5-e4ed77f352ac">IWMPEvents Interface</a>
</li>
<li>
<a href="https://msdn.microsoft.com/61cd0a2e-b94f-4c10-b3e2-ad1dc2a0b17d">IWMPEvents2 Interface</a>
</li>
</ul><table>
<tr>
<td>
<a href="https://msdn.microsoft.com/98970d33-8035-49f9-9243-b4832df6e5c9">Previous</a>
</td>
<td></td>
<td>
<a href="https://msdn.microsoft.com/library/windows/hardware/dn926903">Next</a>
</td>
</tr>
</table> 

