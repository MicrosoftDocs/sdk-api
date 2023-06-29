---
UID: NN:wmsdkidl.IWMDRMMessageParser
title: IWMDRMMessageParser (wmsdkidl.h)
description: The IWMDRMMessageParser interface parses pertinent information from messages received from a device.An IWMDRMMessageParser interface exists for every device registration object.
helpviewer_keywords: ["IWMDRMMessageParser","IWMDRMMessageParser interface [windows Media Format]","IWMDRMMessageParser interface [windows Media Format]","described","IWMDRMMessageParserInterface","wmformat.iwmdrmmessageparser","wmsdkidl/IWMDRMMessageParser"]
old-location: wmformat\iwmdrmmessageparser.htm
tech.root: wmformat
ms.assetid: 76e504e2-5978-4afd-9556-68f78c49a313
ms.date: 4/26/2023
ms.keywords: IWMDRMMessageParser, IWMDRMMessageParser interface [windows Media Format], IWMDRMMessageParser interface [windows Media Format],described, IWMDRMMessageParserInterface, wmformat.iwmdrmmessageparser, wmsdkidl/IWMDRMMessageParser
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMMessageParser
 - wmsdkidl/IWMDRMMessageParser
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmsdkidl.h
api_name:
 - IWMDRMMessageParser
---

# IWMDRMMessageParser interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IWMDRMMessageParser</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMMessageParser</b> interface parses pertinent information from messages received from a device.

An <b>IWMDRMMessageParser</b> interface exists for every device registration object. You can obtain a pointer to this interface by calling the <b>QueryInterface</b> method of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration</a> interface, or any other interface of the device registration object.

## -inheritance

The <b>IWMDRMMessageParser</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDRMMessageParser</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

This interface deals with two types of messages: registration messages that come from new devices on the network, and license request messages that devices send to request actions. These messages are intended to accommodate the Windows Media DRM 10 for Network Devices protocol. A device can send other message types, which your application might need to intercept. Details vary by device and by protocol. For more information, refer to the appropriate specifications or standards for the device or protocol you want to support.

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
