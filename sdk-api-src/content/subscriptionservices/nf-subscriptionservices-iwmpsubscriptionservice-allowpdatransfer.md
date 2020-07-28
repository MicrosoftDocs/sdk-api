---
UID: NF:subscriptionservices.IWMPSubscriptionService.allowPDATransfer
title: IWMPSubscriptionService::allowPDATransfer (subscriptionservices.h)
description: Note  This section describes functionality designed for use by online stores.
helpviewer_keywords: ["IWMPSubscriptionService interface [Windows Media Player]","allowPDATransfer method","IWMPSubscriptionService.allowPDATransfer","IWMPSubscriptionService::allowPDATransfer","IWMPSubscriptionServiceallowPDATransfer","allowPDATransfer","allowPDATransfer method [Windows Media Player]","allowPDATransfer method [Windows Media Player]","IWMPSubscriptionService interface","subscriptionservices/IWMPSubscriptionService::allowPDATransfer","wmp.iwmpsubscriptionservice_allowpdatransfer"]
old-location: wmp\iwmpsubscriptionservice_allowpdatransfer.htm
tech.root: WMP
ms.assetid: a824c6c0-0887-41cb-892a-832635ade222
ms.date: 12/05/2018
ms.keywords: IWMPSubscriptionService interface [Windows Media Player],allowPDATransfer method, IWMPSubscriptionService.allowPDATransfer, IWMPSubscriptionService::allowPDATransfer, IWMPSubscriptionServiceallowPDATransfer, allowPDATransfer, allowPDATransfer method [Windows Media Player], allowPDATransfer method [Windows Media Player],IWMPSubscriptionService interface, subscriptionservices/IWMPSubscriptionService::allowPDATransfer, wmp.iwmpsubscriptionservice_allowpdatransfer
f1_keywords:
- subscriptionservices/IWMPSubscriptionService.allowPDATransfer
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- subscriptionservices.h
api_name:
- IWMPSubscriptionService.allowPDATransfer
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMPSubscriptionService::allowPDATransfer


## -description



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

Do not rely on <b>allowPDATransfer</b> being called each time a track is synchronized with a device. Instead, implement <a href="https://docs.microsoft.com/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice2-prepareforsync">IWMPSubscriptionService2::prepareForSync</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice">IWMPSubscriptionService Interface</a>
 

 

