---
UID: NF:socketapi.SetSocketMediaStreamingMode
title: SetSocketMediaStreamingMode function (socketapi.h)
description: Indicates whether the network is to be used for transferring streaming media that requires quality of service.
helpviewer_keywords: ["SetSocketMediaStreamingMode","SetSocketMediaStreamingMode function [Winsock]","socketapi/SetSocketMediaStreamingMode","winsock.setsocketmediastreamingmode"]
old-location: winsock\setsocketmediastreamingmode.htm
tech.root: WinSock
ms.assetid: 5D1C18FC-2F25-44C0-AD3C-F1E7744C4963
ms.date: 12/05/2018
ms.keywords: SetSocketMediaStreamingMode, SetSocketMediaStreamingMode function [Winsock], socketapi/SetSocketMediaStreamingMode, winsock.setsocketmediastreamingmode
req.header: socketapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Windows.Networking.lib
req.dll: Windows.Networking.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetSocketMediaStreamingMode
 - socketapi/SetSocketMediaStreamingMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.Networking.dll
api_name:
 - SetSocketMediaStreamingMode
---

# SetSocketMediaStreamingMode function


## -description

The 
<b>SetSocketMediaStreamingMode</b> function indicates whether the network is to be used for transferring streaming media that requires quality of service.

## -parameters

### -param value

Indicates whether the network is to be used for transferring streaming media that requires quality of service. This ensures that sockets opened as low latency will get the right quality of service over 802.11 wireless networks.

## -returns

If no error occurs, 
<b>SetSocketMediaStreamingMode</b> returns S_OK. Otherwise, an error code is returned as an HRESULT.

## -remarks

The 
<b>SetSocketMediaStreamingMode</b> function is used to indicate whether the network is to be used for transferring streaming media that requires quality of service. This function is normally used by Voice over IP (VoIP) or similar apps that require a consistent quality of service.  The <b>SetSocketMediaStreamingMode</b> function can be used by Windows Store apps or desktop apps.

There can be quality of service issues for media streaming when used over an 802.11 wireless network. The 802.11 network driver will periodically scan for other nearby infrastructure networks (ESS) or ad-hoc networks (IBSS). This allows the wireless network adapter to find other networks and possibly connected to a network with a stronger signal. Most current 802.11 network drivers scan all of the available channels as a series at once. When the 802.11 network driver is scanning for other networks and listening on other channels, it cannot receive packets for the app. The time spent scanning for other networks can introduce a noticeable gap (100 milliseconds or more)  when a VoIP app would be unable to receive the audio stream. This scanning process is longer for 802.11 network adapters that are dual band (2.4GHz and 5GHz) since even more channels are scanned. This can result in the audio to be perceived as stuttering.

When the <b>SetSocketMediaStreamingMode</b> function is called with the <i>value</i> parameter set to <b>TRUE</b> and the socket will be transferring over an 802.11 wireless network adapter, the system will notify the wireless network driver to stop scanning for other networks. This eliminates stuttering by VoIP and similar audio apps when used over 802.11 wireless networks, but also affects any apps running on the local computer or device. 

There are cases where turning off scans may cause problems. When scans are disabled, the local computer  stays connected to the same network even if the signal becomes weaker and weaker as the user moves away from the network. 

A VoIP or similar app should close all low latency sockets to restore the media streaming mode of the 802.11 wireless network driver. This will re-enable scanning for other wireless networks.

The <b>SetSocketMediaStreamingMode</b> function has no effect if the socket will not be sending or receiving packets over an 802.11 wireless adapter.

## -see-also

<a href="/previous-versions/windows/apps/hh452752(v=win.10)">Adding support for networking</a>



<a href="/uwp/api/windows.networking.backgroundtransfer">Windows.Networking.BackgroundTransfer</a>



<a href="/uwp/api/windows.networking.sockets">Windows.Networking.Sockets</a>