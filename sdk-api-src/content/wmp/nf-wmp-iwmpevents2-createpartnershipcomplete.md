---
UID: NF:wmp.IWMPEvents2.CreatePartnershipComplete
title: IWMPEvents2::CreatePartnershipComplete (wmp.h)
description: The CreatePartnershipComplete event occurs when an asynchronous call to IWMPSyncDevice::createPartnership completes.
helpviewer_keywords: ["CreatePartnershipComplete","CreatePartnershipComplete method [Windows Media Player]","CreatePartnershipComplete method [Windows Media Player]","IWMPEvents2 interface","IWMPEvents2 interface [Windows Media Player]","CreatePartnershipComplete method","IWMPEvents2.CreatePartnershipComplete","IWMPEvents2::CreatePartnershipComplete","IWMPEvents2CreatePartnershipComplete","wmp.iwmpevents2_iwmpevents2__createpartnershipcomplete","wmp/IWMPEvents2::CreatePartnershipComplete"]
old-location: wmp\iwmpevents2_iwmpevents2__createpartnershipcomplete.htm
tech.root: WMP
ms.assetid: 3cd9b27d-ceb4-4655-ab3f-3d341774c81a
ms.date: 12/05/2018
ms.keywords: CreatePartnershipComplete, CreatePartnershipComplete method [Windows Media Player], CreatePartnershipComplete method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],CreatePartnershipComplete method, IWMPEvents2.CreatePartnershipComplete, IWMPEvents2::CreatePartnershipComplete, IWMPEvents2CreatePartnershipComplete, wmp.iwmpevents2_iwmpevents2__createpartnershipcomplete, wmp/IWMPEvents2::CreatePartnershipComplete
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 10 or later.
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
req.dll: Wmp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPEvents2::CreatePartnershipComplete
 - wmp/IWMPEvents2::CreatePartnershipComplete
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents2.CreatePartnershipComplete
---

# IWMPEvents2::CreatePartnershipComplete


## -description

The <b>CreatePartnershipComplete</b> event occurs when an asynchronous call to <b>IWMPSyncDevice::createPartnership</b> completes.

## -parameters

### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device object for which the partnership was created.

### -param hrResult [in]

The success or error <b>HRESULT</b> for the create partnership operation.

## -remarks

A call to <b>IWMPSyncDevice::createPartnership</b> starts the asynchronous operation of creating a partnership between Windows Media Player and a device. This call returns immediately. When the operation that creates the partnership ends, <b>CreatePartnershipComplete</b> occurs.

Receiving this event notification does not guarantee that a partnership exists.

This event is broadcasted to all remoted Windows Media Player control instances.

Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device for which the partnership was created.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership">IWMPSyncDevice::createPartnership</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical">IWMPSyncDevice::isIdentical</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>