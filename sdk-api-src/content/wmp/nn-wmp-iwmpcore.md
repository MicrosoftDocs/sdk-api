---
UID: NN:wmp.IWMPCore
title: IWMPCore (wmp.h)
description: The IWMPCore interface is the root interface for the Windows Media Player control. It can be used to retrieve pointers to other interfaces supported by the control and to access some basic features.helpviewer_keywords: ["IWMPCore","IWMPCore interface [Windows Media Player]","IWMPCore interface [Windows Media Player]","described","IWMPCoreInterface","wmp.iwmpcore","wmp/IWMPCore"]
old-location: wmp\iwmpcore.htm
tech.root: WMP
ms.assetid: 24fbb34d-4a5e-4a00-85fc-9659a31dc650
ms.date: 12/05/2018
ms.keywords: IWMPCore, IWMPCore interface [Windows Media Player], IWMPCore interface [Windows Media Player],described, IWMPCoreInterface, wmp.iwmpcore, wmp/IWMPCore
f1_keywords:
- wmp/IWMPCore
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
- IWMPCore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPCore interface


## -description



The <b>IWMPCore</b> interface is the root interface for the Windows Media Player control. It can be used to retrieve pointers to other interfaces supported by the control and to access some basic features.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPCore</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IWMPCore</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-close">close</a>
</td>
<td align="left" width="63%">
Closes Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection">get_cdromCollection</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPCdromCollection</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_closedcaption">get_closedCaption</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPClosedCaption</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_controls">get_controls</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPControls</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_currentmedia">get_currentMedia</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPMedia</b> interface corresponding to the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_currentplaylist">get_currentPlaylist</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface corresponding to the current playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_error">get_error</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPError</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_isonline">get_isOnline</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the user is connected to a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_mediacollection">get_mediaCollection</a>
</td>
<td align="left" width="63%">
Retrieves pointer to an <b>IWMPMediaCollection</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_network">get_network</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPNetwork</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_openstate">get_openState</a>
</td>
<td align="left" width="63%">
Retrieves an <b>WMPOpenState</b> enumeration value indicating the state of the content source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_playlistcollection">get_playlistCollection</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylistCollection</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_playstate">get_playState</a>
</td>
<td align="left" width="63%">
Retrieves an <b>WMPPlayState</b> enumeration value indicating the operating state of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_settings">get_settings</a>
</td>
<td align="left" width="63%">
Retrieves a pointer an <b>IWMPSettings</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_status">get_status</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the current status of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_url">get_URL</a>
</td>
<td align="left" width="63%">
Retrieves the name of the clip to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_versioninfo">get_versionInfo</a>
</td>
<td align="left" width="63%">
Retrieves a value specifying the version of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-launchurl">launchURL</a>
</td>
<td align="left" width="63%">
Sends a URL to the user's default browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentmedia">put_currentMedia</a>
</td>
<td align="left" width="63%">
Specifies the <b>IWMPMedia</b> interface that corresponds to the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_currentplaylist">put_currentPlaylist</a>
</td>
<td align="left" width="63%">
Specifies the <b>IWMPPlaylist</b> interface that corresponds to the current playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nf-wmp-iwmpcore-put_url">put_URL</a>
</td>
<td align="left" width="63%">
Specifies the name of the clip to play.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection">IWMPCdromCollection Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption">IWMPClosedCaption Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcontrols">IWMPControls Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore2">IWMPCore2 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpcore3">IWMPCore3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmperror">IWMPError Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmedia">IWMPMedia Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection">IWMPMediaCollection Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpnetwork">IWMPNetwork Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplaylist">IWMPPlaylist Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection">IWMPPlaylistCollection Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpsettings">IWMPSettings Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/ne-wmp-wmpopenstate">WMPOpenState</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/ne-wmp-wmpplaystate">WMPPlayState</a>
 

 

