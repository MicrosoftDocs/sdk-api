---
UID: NF:wmp.IWMPEvents2.DeviceSyncError
title: IWMPEvents2::DeviceSyncError (wmp.h)
description: The DeviceSyncError event occurs in response to a synchronization error.
helpviewer_keywords: ["DeviceSyncError","DeviceSyncError method [Windows Media Player]","DeviceSyncError method [Windows Media Player]","IWMPEvents2 interface","IWMPEvents2 interface [Windows Media Player]","DeviceSyncError method","IWMPEvents2.DeviceSyncError","IWMPEvents2::DeviceSyncError","IWMPEvents2DeviceSyncError","wmp.iwmpevents2_iwmpevents2__devicesyncerror","wmp/IWMPEvents2::DeviceSyncError"]
old-location: wmp\iwmpevents2_iwmpevents2__devicesyncerror.htm
tech.root: WMP
ms.assetid: 41e9a6df-3721-4fd2-aa9d-9874a004aa9a
ms.date: 4/26/2023
ms.keywords: DeviceSyncError, DeviceSyncError method [Windows Media Player], DeviceSyncError method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceSyncError method, IWMPEvents2.DeviceSyncError, IWMPEvents2::DeviceSyncError, IWMPEvents2DeviceSyncError, wmp.iwmpevents2_iwmpevents2__devicesyncerror, wmp/IWMPEvents2::DeviceSyncError
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
 - IWMPEvents2::DeviceSyncError
 - wmp/IWMPEvents2::DeviceSyncError
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
 - IWMPEvents2.DeviceSyncError
---

# IWMPEvents2::DeviceSyncError


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DeviceSyncError</b> event occurs in response to a synchronization error.

## -parameters

### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device for which the synchronization error occurred.

### -param pMedia [in]

Address of the <b>IWMPDispatch</b> interface that represents the media item for which the synchronization error occurred.

## -remarks

You should call <b>QueryInterface</b> on <i>pMedia</i> to get the <b>IWMPMedia2</b> interface for the <b>Media</b> object. You can then use <b>IWMPMedia2::get_error</b> to retrieve more information about the error that occurred.

Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device for which the error occurred.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="/windows/desktop/api/wmp/nn-wmp-iwmpmedia2">IWMPMedia2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical">IWMPSyncDevice::isIdentical</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>