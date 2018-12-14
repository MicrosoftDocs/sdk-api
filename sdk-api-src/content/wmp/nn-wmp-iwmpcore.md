---
UID: NN:wmp.IWMPCore
title: IWMPCore
author: windows-sdk-content
description: The IWMPCore interface is the root interface for the Windows Media Player control. It can be used to retrieve pointers to other interfaces supported by the control and to access some basic features.
old-location: wmp\iwmpcore.htm
tech.root: WMP
ms.assetid: 24fbb34d-4a5e-4a00-85fc-9659a31dc650
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWMPCore, IWMPCore interface [Windows Media Player], IWMPCore interface [Windows Media Player],described, IWMPCoreInterface, wmp.iwmpcore, wmp/IWMPCore
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMPCore
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPCore interface


## -description



The <b>IWMPCore</b> interface is the root interface for the Windows Media Player control. It can be used to retrieve pointers to other interfaces supported by the control and to access some basic features.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPCore</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IWMPCore</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMPCore</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563223(v=VS.85).aspx">close</a>
</td>
<td align="left" width="63%">
Closes Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563224(v=VS.85).aspx">get_cdromCollection</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPCdromCollection</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563225(v=VS.85).aspx">get_closedCaption</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPClosedCaption</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563226(v=VS.85).aspx">get_controls</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPControls</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563227(v=VS.85).aspx">get_currentMedia</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPMedia</b> interface corresponding to the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563228(v=VS.85).aspx">get_currentPlaylist</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface corresponding to the current playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563229(v=VS.85).aspx">get_error</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPError</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563230(v=VS.85).aspx">get_isOnline</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the user is connected to a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563231(v=VS.85).aspx">get_mediaCollection</a>
</td>
<td align="left" width="63%">
Retrieves pointer to an <b>IWMPMediaCollection</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563232(v=VS.85).aspx">get_network</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPNetwork</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563233(v=VS.85).aspx">get_openState</a>
</td>
<td align="left" width="63%">
Retrieves an <b>WMPOpenState</b> enumeration value indicating the state of the content source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563234(v=VS.85).aspx">get_playlistCollection</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylistCollection</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563235(v=VS.85).aspx">get_playState</a>
</td>
<td align="left" width="63%">
Retrieves an <b>WMPPlayState</b> enumeration value indicating the operating state of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563236(v=VS.85).aspx">get_settings</a>
</td>
<td align="left" width="63%">
Retrieves a pointer an <b>IWMPSettings</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563237(v=VS.85).aspx">get_status</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the current status of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563238(v=VS.85).aspx">get_URL</a>
</td>
<td align="left" width="63%">
Retrieves the name of the clip to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563239(v=VS.85).aspx">get_versionInfo</a>
</td>
<td align="left" width="63%">
Retrieves a value specifying the version of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563240(v=VS.85).aspx">launchURL</a>
</td>
<td align="left" width="63%">
Sends a URL to the user's default browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563241(v=VS.85).aspx">put_currentMedia</a>
</td>
<td align="left" width="63%">
Specifies the <b>IWMPMedia</b> interface that corresponds to the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563242(v=VS.85).aspx">put_currentPlaylist</a>
</td>
<td align="left" width="63%">
Specifies the <b>IWMPPlaylist</b> interface that corresponds to the current playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd563243(v=VS.85).aspx">put_URL</a>
</td>
<td align="left" width="63%">
Specifies the name of the clip to play.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563097(v=VS.85).aspx">IWMPCdromCollection Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563113(v=VS.85).aspx">IWMPClosedCaption Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563179(v=VS.85).aspx">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563217(v=VS.85).aspx">IWMPCore2 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563219(v=VS.85).aspx">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563272(v=VS.85).aspx">IWMPError Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563397(v=VS.85).aspx">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563405(v=VS.85).aspx">IWMPMediaCollection Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563461(v=VS.85).aspx">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563547(v=VS.85).aspx">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563552(v=VS.85).aspx">IWMPPlaylistCollection Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563648(v=VS.85).aspx">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd">Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd564878(v=VS.85).aspx">WMPOpenState</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd564881(v=VS.85).aspx">WMPPlayState</a>
 

 

