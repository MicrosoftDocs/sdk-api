---
UID: NF:qnetwork.IAMNetworkStatus.get_LostPackets
title: IAMNetworkStatus::get_LostPackets
author: windows-driver-content
description: The get_LostPackets method retrieves the number of packets that have been lost.
old-location: dshow\iamnetworkstatus_get_lostpackets.htm
old-project: DirectShow
ms.assetid: 814a2ffa-c7f3-47e6-8956-4a705b394469
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAMNetworkStatus interface [DirectShow],get_LostPackets method, IAMNetworkStatus.get_LostPackets, IAMNetworkStatus::get_LostPackets, IAMNetworkStatusget_LostPackets, dshow.iamnetworkstatus_get_lostpackets, get_LostPackets, get_LostPackets method [DirectShow], get_LostPackets method [DirectShow],IAMNetworkStatus interface, qnetwork/IAMNetworkStatus::get_LostPackets
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Qnetwork.h
api_name:
-	IAMNetworkStatus.get_LostPackets
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAMNetworkStatus::get_LostPackets


## -description



The <code>get_LostPackets</code> method retrieves the number of packets that have been lost.




## -parameters




### -param pLostPackets

Pointer to a variable that receives the number of lost packets.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This property is only valid for streaming media, and will equal zero when using the HTTP protocol, which is lossless. Packets may be lost for a number of reasons, such as the type and quality of the network connection.

Whenever playback is stopped and restarted, this property is set to zero. It is not reset if playback is paused and restarted.




## -see-also




<a href="https://msdn.microsoft.com/51d56b76-f9fc-44e1-88f0-d35d861a4697">IAMNetworkStatus Interface</a>
 

 

