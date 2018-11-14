---
UID: NN:wmsdkidl.IWMDRMMessageParser
title: IWMDRMMessageParser
author: windows-sdk-content
description: The IWMDRMMessageParser interface parses pertinent information from messages received from a device.An IWMDRMMessageParser interface exists for every device registration object.
old-location: wmformat\iwmdrmmessageparser.htm
tech.root: wmformat
ms.assetid: 76e504e2-5978-4afd-9556-68f78c49a313
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWMDRMMessageParser, IWMDRMMessageParser interface [windows Media Format], IWMDRMMessageParser interface [windows Media Format],described, IWMDRMMessageParserInterface, wmformat.iwmdrmmessageparser, wmsdkidl/IWMDRMMessageParser
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMDRMMessageParser
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMDRMMessageParser interface


## -description


<p class="CCE_Message">[<b>IWMDRMMessageParser</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="http://go.microsoft.com/fwlink/p/?linkid=325240">Microsoft PlayReady</a>.
]


The <b>IWMDRMMessageParser</b> interface parses pertinent information from messages received from a device.

An <b>IWMDRMMessageParser</b> interface exists for every device registration object. You can obtain a pointer to this interface by calling the <b>QueryInterface</b> method of the <a href="https://msdn.microsoft.com/fb08ddae-2abf-4a86-a5d8-ea745ae35aa8">IWMDeviceRegistration</a> interface, or any other interface of the device registration object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMMessageParser</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMDRMMessageParser</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMDRMMessageParser</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d51b7f7-5cc2-4dbd-8a61-2901c01734bb">ParseLicenseRequestMsg</a>
</td>
<td align="left" width="63%">
Parses a license request message from a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d2d142bf-0fed-42c8-a2f1-b539a40ac074">ParseRegistrationReqMsg</a>
</td>
<td align="left" width="63%">
Parses a registration request from a device.

</td>
</tr>
</table> 


## -remarks



This interface deals with two types of messages: registration messages that come from new devices on the network, and license request messages that devices send to request actions. These messages are intended to accommodate the Windows Media DRM 10 for Network Devices protocol. A device can send other message types, which your application might need to intercept. Details vary by device and by protocol. For more information, refer to the appropriate specifications or standards for the device or protocol you want to support.




## -see-also




<a href="https://msdn.microsoft.com/c61a0739-09f2-497f-a2cd-d3f2472738e3">Interfaces</a>
 

 

