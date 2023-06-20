---
UID: NN:wmp.IWMPEvents3
title: IWMPEvents3 (wmp.h)
description: The IWMPEvents3 interface provides access to events originating from the Windows Media Player 11 control so that an application that has this control embedded in it can respond to these events.
helpviewer_keywords: ["IWMPEvents3","IWMPEvents3 interface [Windows Media Player]","IWMPEvents3 interface [Windows Media Player]","described","IWMPEvents3Interface","wmp.iwmpevents3","wmp/IWMPEvents3"]
old-location: wmp\iwmpevents3.htm
tech.root: WMP
ms.assetid: 654b7d78-97d4-4770-9729-dd1fed0431d9
ms.date: 4/26/2023
ms.keywords: IWMPEvents3, IWMPEvents3 interface [Windows Media Player], IWMPEvents3 interface [Windows Media Player],described, IWMPEvents3Interface, wmp.iwmpevents3, wmp/IWMPEvents3
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents3
 - wmp/IWMPEvents3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPEvents3
---

# IWMPEvents3 interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPEvents3</b> interface provides access to events originating from the Windows Media Player 11 control so that an application that has this control embedded in it can respond to these events. The events exposed by <b>IWMPEvents3</b> are also exposed by the <a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents</a> interface.



The events provided by <b>IWMPEvents3</b> extend the set of events provided by <a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents</a> and <a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2</a> by adding events related to CD ripping, CD burning, folder monitoring, and remote library services.

In addition to the methods inherited from <a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2</a>, the <b>IWMPEvents3</b> interface exposes the following methods.
<table>
<tr>
<th>Method
          </th>
<th>Description
          </th>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror">CdromBurnError</a>
</td>
<td>Occurs when a generic error happens during a CD burning operation.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror">CdromBurnMediaError</a>
</td>
<td>Occurs when an error happens while burning an individual media item to a CD.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange">CdromBurnStateChange</a>
</td>
<td>Occurs when a CD burning operation changes state.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror">CdromRipMediaError</a>
</td>
<td>Occurs when an error happens while ripping an individual track from a CD.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange">CdromRipStateChange</a>
</td>
<td>Occurs when a CD ripping operation changes state.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-folderscanstatechange">FolderScanStateChange</a>
</td>
<td>Occurs when a folder monitoring operation changes state.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-libraryconnect">LibraryConnect</a>
</td>
<td>Occurs when a library becomes available.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-librarydisconnect">LibraryDisconnect</a>
</td>
<td>Occurs when a library is no longer available.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-mediacollectionmediaadded">MediaCollectionMediaAdded</a>
</td>
<td>Occurs when a media item is added to the local library.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-mediacollectionmediaremoved">MediaCollectionMediaRemoved</a>
</td>
<td>Occurs when a media item is removed from the local library.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-stringcollectionchange">StringCollectionChange</a>
</td>
<td>Occurs when a string collection changes.</td>
</tr>
</table> 
<ul>
<li>
<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>
</li>
<li>
<a href="/windows/desktop/WMP/handling-events-in-c">Handling Events in C++</a>
</li>
<li>
<a href="/windows/desktop/WMP/interfaces">Interfaces</a>
</li>
<li>
<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents">IWMPEvents Interface</a>
</li>
<li>
<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>
</li>
</ul><table>
<tr>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents2-devicesyncstatechange">Previous</a>
</td>
<td></td>
<td>
<a href="/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror">Next</a>
</td>
</tr>
</table>