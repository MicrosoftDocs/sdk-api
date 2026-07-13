---
UID: NF:subscriptionservices.IWMPSubscriptionService.allowPDATransfer
title: IWMPSubscriptionService::allowPDATransfer (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionService interface [Windows Media Player]","allowPDATransfer method","IWMPSubscriptionService.allowPDATransfer","IWMPSubscriptionService::allowPDATransfer","IWMPSubscriptionServiceallowPDATransfer","allowPDATransfer","allowPDATransfer method [Windows Media Player]","allowPDATransfer method [Windows Media Player]","IWMPSubscriptionService interface","subscriptionservices/IWMPSubscriptionService::allowPDATransfer","wmp.iwmpsubscriptionservice_allowpdatransfer"]
old-location: wmp\iwmpsubscriptionservice_allowpdatransfer.htm
tech.root: WMP
ms.assetid: a824c6c0-0887-41cb-892a-832635ade222
ms.date: 4/26/2023
ms.keywords: IWMPSubscriptionService interface [Windows Media Player],allowPDATransfer method, IWMPSubscriptionService.allowPDATransfer, IWMPSubscriptionService::allowPDATransfer, IWMPSubscriptionServiceallowPDATransfer, allowPDATransfer, allowPDATransfer method [Windows Media Player], allowPDATransfer method [Windows Media Player],IWMPSubscriptionService interface, subscriptionservices/IWMPSubscriptionService::allowPDATransfer, wmp.iwmpsubscriptionservice_allowpdatransfer
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
 - IWMPSubscriptionService::allowPDATransfer
 - subscriptionservices/IWMPSubscriptionService::allowPDATransfer
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
 - IWMPSubscriptionService.allowPDATransfer
---

# IWMPSubscriptionService::allowPDATransfer


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>allowPDATransfer</b> method is implemented by the online store's plug-in to manage permission for Windows Media Player to synchronize content with a device.

## -parameters

### -param hwnd [in]

A handle to a window in which the plug-in can display a user interface.

### -param pPlaylist [in, out]

Pointer to a playlist object.

### -param pfAllowTransfer [out]

Pointer to a <b>BOOL</b>. If true, copying to a device is allowed.

## -returns

The method returns an <b>HRESULT</b>.

## -remarks

Your code should not perform lengthy operations synchronously when Windows Media Player calls this method.

When Windows Media Player calls your plug-in's <b>allowPDATransfer</b> method, it passes a pointer to a playlist, which contains items from your online store. Your <b>allowPDATransfer</b> method must remove any items from the playlist that should not be synchronized with a device.

The situations in which Windows Media Player calls <b>allowPDATranfer</b> differ between versions of Windows Media Player.

Windows Media Player 9 Series and Windows Media Player 10 call <b>allowPDATransfer</b> automatically in certain situations. For example, if the user attempts to synchronize a list of tracks with a device, and some of those tracks do not have permission to be synchronized, Windows Media Player calls <b>allowPDATransfer</b>.

Windows Media Player 11 never calls <b>allowPDATransfer</b> automatically. That is, Windows Media Player 11 calls <b>allowPDATransfer</b> only when the user explicitly requests synchronization rights. For example, the user might request a synchronization rights by choosing a command from the context menu of an information icon.

Do not rely on <b>allowPDATransfer</b> being called each time a track is synchronized with a device. Instead, implement <a href="/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync">IWMPSubscriptionService2::prepareForSync</a>.

## -see-also

<a href="/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice">IWMPSubscriptionService Interface</a>