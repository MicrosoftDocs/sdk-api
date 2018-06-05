---
UID: NN:wmp.IWMPCore
title: IWMPCore
author: windows-sdk-content
description: The IWMPCore interface is the root interface for the Windows Media Player control. It can be used to retrieve pointers to other interfaces supported by the control and to access some basic features.
old-location: wmp\iwmpcore.htm
old-project: WMP
ms.assetid: 24fbb34d-4a5e-4a00-85fc-9659a31dc650
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPCore, IWMPCore interface [Windows Media Player], IWMPCore interface [Windows Media Player],described, IWMPCoreInterface, wmp.iwmpcore, wmp/IWMPCore
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.h
api_name:
-	IWMPCore
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPCore interface


## -description



The <b>IWMPCore</b> interface is the root interface for the Windows Media Player control. It can be used to retrieve pointers to other interfaces supported by the control and to access some basic features.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMPCore</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IWMPCore</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">close</a>
</td>
<td align="left" width="63%">
Closes Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6bb6500e-7a30-400b-a88b-7ee3596501b1">get_cdromCollection</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPCdromCollection</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f170430-2ce4-490b-9163-f39221a8db5c">get_closedCaption</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPClosedCaption</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54d013f1-d71b-4b6a-90b4-0226022a2a0f">get_controls</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPControls</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4f199336-0555-40de-8d27-780b05ef9510">get_currentMedia</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPMedia</b> interface corresponding to the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb923325-67d2-4d73-b7ec-49e9b52cabba">get_currentPlaylist</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylist</b> interface corresponding to the current playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db00797b-989f-4f92-8fac-aaa147e37383">get_error</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPError</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5507a80f-4bef-4712-af41-49e58d8396aa">get_isOnline</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating whether the user is connected to a network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41b090ca-edf0-440e-b578-26c5ad064657">get_mediaCollection</a>
</td>
<td align="left" width="63%">
Retrieves pointer to an <b>IWMPMediaCollection</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8100008a-50da-4496-9d5a-77bcca94e903">get_network</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPNetwork</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/66c7e52a-d7b4-4c37-a863-fb42f5415c0a">get_openState</a>
</td>
<td align="left" width="63%">
Retrieves an <b>WMPOpenState</b> enumeration value indicating the state of the content source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8f6ab34f-e055-4a18-b1b8-e3c7b8f9c76a">get_playlistCollection</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to an <b>IWMPPlaylistCollection</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cadac1c6-fff6-44aa-a6ce-2b2f69da2d78">get_playState</a>
</td>
<td align="left" width="63%">
Retrieves an <b>WMPPlayState</b> enumeration value indicating the operating state of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bbffaff-99e4-4aae-9b8f-cdb86648fdd9">get_settings</a>
</td>
<td align="left" width="63%">
Retrieves a pointer an <b>IWMPSettings</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee11cb36-4dd2-4fe4-84fd-b3fc11b13ae0">get_status</a>
</td>
<td align="left" width="63%">
Retrieves a value indicating the current status of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/54d43a1c-807a-40a5-a703-262d75f88ca0">get_URL</a>
</td>
<td align="left" width="63%">
Retrieves the name of the clip to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8c8bb30b-8f8e-4f49-9506-d4735bccf847">get_versionInfo</a>
</td>
<td align="left" width="63%">
Retrieves a value specifying the version of Windows Media Player.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/439bb4a7-801a-4bef-b791-b8a9cb24ab34">launchURL</a>
</td>
<td align="left" width="63%">
Sends a URL to the user's default browser.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/003d1937-13f0-4d2c-ad5c-a83569295b62">put_currentMedia</a>
</td>
<td align="left" width="63%">
Specifies the <b>IWMPMedia</b> interface that corresponds to the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/943641ca-9733-4066-bc69-834e792d93dc">put_currentPlaylist</a>
</td>
<td align="left" width="63%">
Specifies the <b>IWMPPlaylist</b> interface that corresponds to the current playlist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0a8625b9-19a1-41dc-9bb8-afca4bfebf5a">put_URL</a>
</td>
<td align="left" width="63%">
Specifies the name of the clip to play.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ba55ac32-149d-4f7b-a2bb-1fdb0be806cd">IWMPCdromCollection Interface</a>



<a href="https://msdn.microsoft.com/fd67e139-0bc1-459e-b43b-bf07f6f656ed">IWMPClosedCaption Interface</a>



<a href="https://msdn.microsoft.com/422ac0d8-8e94-4484-802f-cdf4ae482fa8">IWMPControls Interface</a>



<a href="https://msdn.microsoft.com/5f839bfe-bf67-49eb-8743-57713e1be7c5">IWMPCore2 Interface</a>



<a href="https://msdn.microsoft.com/3004551e-ce36-4f15-88c3-93b2bfaa72fc">IWMPCore3 Interface</a>



<a href="https://msdn.microsoft.com/f22759cd-0ca7-4992-bb17-0272b35d6d75">IWMPError Interface</a>



<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection Interface</a>



<a href="https://msdn.microsoft.com/074a4bc2-3d9f-4007-b6c8-91ea92a87b67">IWMPNetwork Interface</a>



<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/b6861651-f0c3-4b99-8c81-a8a8f8b47692">IWMPPlaylistCollection Interface</a>



<a href="https://msdn.microsoft.com/e5a305a1-958e-4b6d-bb1f-f00bf5eb08dd">IWMPSettings Interface</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>



<a href="https://msdn.microsoft.com/535c8f56-d854-449b-ad50-72e5dd32710a">WMPOpenState</a>



<a href="https://msdn.microsoft.com/15787d18-bc38-4fc7-a920-539d66252035">WMPPlayState</a>
 

 

