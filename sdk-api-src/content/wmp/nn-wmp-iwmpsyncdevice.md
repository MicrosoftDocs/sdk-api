---
UID: NN:wmp.IWMPSyncDevice
title: IWMPSyncDevice (wmp.h)
description: The IWMPSyncDevice interface represents a device to which Windows Media Player 10 or later can copy digital media files.
helpviewer_keywords: ["IWMPSyncDevice","IWMPSyncDevice interface [Windows Media Player]","IWMPSyncDevice interface [Windows Media Player]","described","IWMPSyncDeviceInterface","wmp.iwmpsyncdevice","wmp/IWMPSyncDevice"]
old-location: wmp\iwmpsyncdevice.htm
tech.root: WMP
ms.assetid: 981648e4-0cb1-4d7a-bd3b-50e1b9a7282c
ms.date: 4/26/2023
ms.keywords: IWMPSyncDevice, IWMPSyncDevice interface [Windows Media Player], IWMPSyncDevice interface [Windows Media Player],described, IWMPSyncDeviceInterface, wmp.iwmpsyncdevice, wmp/IWMPSyncDevice
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMPSyncDevice
 - wmp/IWMPSyncDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.h
api_name:
 - IWMPSyncDevice
---

# IWMPSyncDevice interface


## -description

\[The feature associated with this page, [Windows Media Player SDK](/windows/win32/wmp/windows-media-player-sdk), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer). **MediaPlayer** has been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** instead of **Windows Media Player SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IWMPSyncDevice</b> interface represents a device to which Windows Media Player 10 or later can copy digital media files. It provides methods used to specify and retrieve properties for the device and to manage the relationship between Windows Media Player and the device.

To use this interface, you must create a remoted instance of the Windows Media Player 10 or later control.

## -inheritance

The <b>IWMPSyncDevice</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMPSyncDevice</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -see-also

<a href="/windows/desktop/WMP/interfaces">Interfaces</a>



<a href="/windows/desktop/WMP/remoting-the-windows-media-player-control">Remoting the Windows Media Player Control</a>
