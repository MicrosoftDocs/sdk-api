---
UID: NF:wmp.IWMPEvents2.DeviceSyncStateChange
title: IWMPEvents2::DeviceSyncStateChange (wmp.h)
description: The DeviceSyncStateChange event occurs when the synchronization state of a device changes.
helpviewer_keywords: ["DeviceSyncStateChange","DeviceSyncStateChange method [Windows Media Player]","DeviceSyncStateChange method [Windows Media Player]","IWMPEvents2 interface","IWMPEvents2 interface [Windows Media Player]","DeviceSyncStateChange method","IWMPEvents2.DeviceSyncStateChange","IWMPEvents2::DeviceSyncStateChange","IWMPEvents2DeviceSyncStateChange","wmp.iwmpevents2_iwmpevents2__devicesyncstatechange","wmp/IWMPEvents2::DeviceSyncStateChange"]
old-location: wmp\iwmpevents2_iwmpevents2__devicesyncstatechange.htm
tech.root: WMP
ms.assetid: 98970d33-8035-49f9-9243-b4832df6e5c9
ms.date: 4/26/2023
ms.keywords: DeviceSyncStateChange, DeviceSyncStateChange method [Windows Media Player], DeviceSyncStateChange method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceSyncStateChange method, IWMPEvents2.DeviceSyncStateChange, IWMPEvents2::DeviceSyncStateChange, IWMPEvents2DeviceSyncStateChange, wmp.iwmpevents2_iwmpevents2__devicesyncstatechange, wmp/IWMPEvents2::DeviceSyncStateChange
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
 - IWMPEvents2::DeviceSyncStateChange
 - wmp/IWMPEvents2::DeviceSyncStateChange
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
 - IWMPEvents2.DeviceSyncStateChange
---

# IWMPEvents2::DeviceSyncStateChange


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DeviceSyncStateChange</b> event occurs when the synchronization state of a device changes.

## -parameters

### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device for which the synchronization state changed.

### -param NewState [in]

<b>WMPSyncState</b> enumeration value that represents the new synchronization state for the device specified by <i>pDevice</i>.

## -remarks

Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device for which the synchronization state changed.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical">IWMPSyncDevice::isIdentical</a>



<a href="/windows/desktop/api/wmp/ne-wmp-wmpsyncstate">WMPSyncState</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>