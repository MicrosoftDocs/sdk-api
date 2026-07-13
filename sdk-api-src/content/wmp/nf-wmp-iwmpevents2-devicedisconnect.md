---
UID: NF:wmp.IWMPEvents2.DeviceDisconnect
title: IWMPEvents2::DeviceDisconnect (wmp.h)
description: The DeviceDisconnect event occurs when the user disconnects a device from the computer.
helpviewer_keywords: ["DeviceDisconnect","DeviceDisconnect method [Windows Media Player]","DeviceDisconnect method [Windows Media Player]","IWMPEvents2 interface","IWMPEvents2 interface [Windows Media Player]","DeviceDisconnect method","IWMPEvents2.DeviceDisconnect","IWMPEvents2::DeviceDisconnect","IWMPEvents2DeviceDisconnect","wmp.iwmpevents2_iwmpevents2__devicedisconnect","wmp/IWMPEvents2::DeviceDisconnect"]
old-location: wmp\iwmpevents2_iwmpevents2__devicedisconnect.htm
tech.root: WMP
ms.assetid: a37b72f9-4f71-433c-afad-66caae2d749a
ms.date: 4/26/2023
ms.keywords: DeviceDisconnect, DeviceDisconnect method [Windows Media Player], DeviceDisconnect method [Windows Media Player],IWMPEvents2 interface, IWMPEvents2 interface [Windows Media Player],DeviceDisconnect method, IWMPEvents2.DeviceDisconnect, IWMPEvents2::DeviceDisconnect, IWMPEvents2DeviceDisconnect, wmp.iwmpevents2_iwmpevents2__devicedisconnect, wmp/IWMPEvents2::DeviceDisconnect
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
 - IWMPEvents2::DeviceDisconnect
 - wmp/IWMPEvents2::DeviceDisconnect
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
 - IWMPEvents2.DeviceDisconnect
---

# IWMPEvents2::DeviceDisconnect


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>DeviceDisconnect</b> event occurs when the user disconnects a device from the computer.

## -parameters

### -param pDevice [in]

Address of the <b>IWMPSyncDevice</b> interface that represents the device that the user disconnected.

## -remarks

Use <b>IWMPSyncDevice::isIdentical</b> to determine whether a particular device matches the device that the user disconnected.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.

## -see-also

<a href="/windows/desktop/api/wmp/nn-wmp-iwmpevents2">IWMPEvents2 Interface</a>



<a href="/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-isidentical">IWMPSyncDevice::isIdentical</a>



<a href="/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>