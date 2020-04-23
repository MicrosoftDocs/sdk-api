---
UID: NN:wmsdkidl.IWMDRMMessageParser
title: IWMDRMMessageParser (wmsdkidl.h)
description: The IWMDRMMessageParser interface parses pertinent information from messages received from a device.An IWMDRMMessageParser interface exists for every device registration object.helpviewer_keywords: ["IWMDRMMessageParser","IWMDRMMessageParser interface [windows Media Format]","IWMDRMMessageParser interface [windows Media Format]","described","IWMDRMMessageParserInterface","wmformat.iwmdrmmessageparser","wmsdkidl/IWMDRMMessageParser"]
old-location: wmformat\iwmdrmmessageparser.htm
tech.root: wmformat
ms.assetid: 76e504e2-5978-4afd-9556-68f78c49a313
ms.date: 12/05/2018
ms.keywords: IWMDRMMessageParser, IWMDRMMessageParser interface [windows Media Format], IWMDRMMessageParser interface [windows Media Format],described, IWMDRMMessageParserInterface, wmformat.iwmdrmmessageparser, wmsdkidl/IWMDRMMessageParser
f1_keywords:
- wmsdkidl/IWMDRMMessageParser
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMDRMMessageParser interface


## -description


<p class="CCE_Message">[<b>IWMDRMMessageParser</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMMessageParser</b> interface parses pertinent information from messages received from a device.

An <b>IWMDRMMessageParser</b> interface exists for every device registration object. You can obtain a pointer to this interface by calling the <b>QueryInterface</b> method of the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration</a> interface, or any other interface of the device registration object.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMDRMMessageParser</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDRMMessageParser</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg">ParseLicenseRequestMsg</a>
</td>
<td align="left" width="63%">
Parses a license request message from a device.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parseregistrationreqmsg">ParseRegistrationReqMsg</a>
</td>
<td align="left" width="63%">
Parses a registration request from a device.

</td>
</tr>
</table> 


## -remarks



This interface deals with two types of messages: registration messages that come from new devices on the network, and license request messages that devices send to request actions. These messages are intended to accommodate the Windows Media DRM 10 for Network Devices protocol. A device can send other message types, which your application might need to intercept. Details vary by device and by protocol. For more information, refer to the appropriate specifications or standards for the device or protocol you want to support.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/wmformat/interfaces">Interfaces</a>
 

 

