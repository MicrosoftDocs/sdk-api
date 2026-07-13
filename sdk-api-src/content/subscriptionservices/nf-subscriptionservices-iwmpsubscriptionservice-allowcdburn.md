---
UID: NF:subscriptionservices.IWMPSubscriptionService.allowCDBurn
title: IWMPSubscriptionService::allowCDBurn (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionService interface [Windows Media Player]","allowCDBurn method","IWMPSubscriptionService.allowCDBurn","IWMPSubscriptionService::allowCDBurn","IWMPSubscriptionServiceallowCDBurn","allowCDBurn","allowCDBurn method [Windows Media Player]","allowCDBurn method [Windows Media Player]","IWMPSubscriptionService interface","subscriptionservices/IWMPSubscriptionService::allowCDBurn","wmp.iwmpsubscriptionservice_allowcdburn"]
old-location: wmp\iwmpsubscriptionservice_allowcdburn.htm
tech.root: WMP
ms.assetid: a17ab1c3-8208-481f-8566-164e2d817e05
ms.date: 4/26/2023
ms.keywords: IWMPSubscriptionService interface [Windows Media Player],allowCDBurn method, IWMPSubscriptionService.allowCDBurn, IWMPSubscriptionService::allowCDBurn, IWMPSubscriptionServiceallowCDBurn, allowCDBurn, allowCDBurn method [Windows Media Player], allowCDBurn method [Windows Media Player],IWMPSubscriptionService interface, subscriptionservices/IWMPSubscriptionService::allowCDBurn, wmp.iwmpsubscriptionservice_allowcdburn
req.header: subscriptionservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
 - IWMPSubscriptionService::allowCDBurn
 - subscriptionservices/IWMPSubscriptionService::allowCDBurn
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - subscriptionservices.h
api_name:
 - IWMPSubscriptionService.allowCDBurn
---

# IWMPSubscriptionService::allowCDBurn


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>allowCDBurn</b> method is implemented by the online store's plug-in to manage permission for Windows Media Player to copy content to a CD.

## -parameters

### -param hwnd [in]

A handle to a window in which the plug-in can display a user interface.

### -param pPlaylist [in, out]

Pointer to a playlist object. The plug-in must remove from the playlist any media item that does not have a current license that includes burn rights.

### -param pfAllowBurn [out]

Pointer to a <b>BOOL</b>. If true, copying to CD is allowed for the media items that remain in the playlist.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

The situations in which Windows Media Player calls <b>allowCDBurn</b> differ between versions of Windows Media Player.

Windows Media Player 9 Series and Windows Media Player 10 call <b>allowCDBurn</b> automatically when the user attempts to burn a list of media items to a CD, and the Player passes the entire list in the <i>pPlaylist</i> parameter. The <b>allowCDBurn</b> method removes from the playlist any media items that do not have a current license. Then the <b>allowCDBurn</b> method can initiate license renewal, on a background thread, for media items that do not have current licenses. The <b>allowCDBurn</b> method must not wait for the background thread to complete the license renewal. Instead, it must return as soon as it has initiated the renewal.

Windows Media Player 11 never calls <b>allowCDBurn</b> automatically. That is, Windows Media Player 11 calls <b>allowCDBurn</b> only when the user explicitly requests burn rights. When the user attempts to burn a list of media items to a CD, Windows Media Player checks to see whether those items have current licenses that include burn rights. For each item that does not have a current license, the Player displays an information icon, which has a context menu. The context menu lets the user request burn rights for the individual media item or for all media items in the basket from the same online store that do not already have burn rights. If the user requests burn rights by choosing a command from the context menu, the Player calls <b>allowCDBurn</b>, passing a playlist that contains the media items for which the user is requesting rights. The <b>allowCDBurn</b> method can then initiate license renewal on a background thread. The <b>allowCDBurn</b> method must not wait for the background thread to complete the license renewal. Instead, it must return as soon as it has initiated the renewal.

Note that Windows Media Player 11 ignores the playlist and the Boolean value that <b>allowCDBurn</b> returns in the <i>pPlaylist</i> and <i>pfAllowBurn</i> parameters. Also note that because of the way Windows Media Player 11 handles burn rights, you must not rely on <b>allowCDBurn</b> being called each time a track is burned to a CD.

Regardless of the Player version, there is no callback mechanism that the background thread can use to notify Windows Media Player that a license renewal is complete. However, if the license renewal for a media item succeeds, then the next time the user attempts to copy the item to a CD, the copy will succeed.

## -see-also

<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice">IWMPSubscriptionService Interface</a>