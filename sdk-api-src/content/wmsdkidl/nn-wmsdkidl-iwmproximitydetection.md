---
UID: NN:wmsdkidl.IWMProximityDetection
title: IWMProximityDetection
author: windows-driver-content
description: The IWMProximityDetection interface validates a playback device for receiving media data.
old-location: wmformat\iwmproximitydetection.htm
old-project: wmformat
ms.assetid: 0897ad8f-8e06-4de9-840e-1588e0e20c54
ms.author: windowsdriverdev
ms.date: 4/13/2018
ms.keywords: IWMProximityDetection, IWMProximityDetection interface [windows Media Format], IWMProximityDetection interface [windows Media Format], described, IWMProximityDetectionInterface, wmformat.iwmproximitydetection, wmsdkidl/IWMProximityDetection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wmsdkidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmsdkidl.h
api_name:
-	IWMProximityDetection
product: Windows
targetos: Windows
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMProximityDetection interface


## -description


<p class="CCE_Message">[<b>IWMProximityDetection</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMProximityDetection</b> interface validates a playback device for receiving media data. The validation process confirms that the device is "near" enough on the network to receive media through the Windows Media DRM 10 for Network Devices protocol.

An <b>IWMProximityDetection</b> interface exists for every device registration object. You can obtain a pointer to this interface by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/fb08ddae-2abf-4a86-a5d8-ea745ae35aa8">IWMDeviceRegistration</a> interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMProximityDetection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMProximityDetection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMProximityDetection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90db4712-cf3e-4526-b07b-ea74c521dbc3">StartDetection</a>
</td>
<td align="left" width="63%">
Initiates proximity detection.

</td>
</tr>
</table> 


## -remarks



The validation state is stored in the device registration database. You can check the validation state for a device by calling <a href="https://msdn.microsoft.com/ce09e6ad-10c0-4cdd-8dee-4faacd958f2b">IWMRegisteredDevice::IsValid</a>.

Validation expires after 48 hours.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

