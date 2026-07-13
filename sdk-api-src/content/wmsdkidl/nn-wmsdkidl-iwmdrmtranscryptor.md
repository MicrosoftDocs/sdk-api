---
UID: NN:wmsdkidl.IWMDRMTranscryptor
title: IWMDRMTranscryptor (wmsdkidl.h)
description: The IWMDRMTranscryptor interface transforms a DRM-protected ASF file into a secure data stream conforming to the Windows Media DRM 10 for Network Devices protocol.
helpviewer_keywords: ["IWMDRMTranscryptor","IWMDRMTranscryptor interface [windows Media Format]","IWMDRMTranscryptor interface [windows Media Format]","described","IWMDRMTranscryptorInterface","wmformat.iwmdrmtranscryptor","wmsdkidl/IWMDRMTranscryptor"]
old-location: wmformat\iwmdrmtranscryptor.htm
tech.root: wmformat
ms.assetid: cd154077-eebe-4a0f-ae70-5268d5af4898
ms.date: 4/26/2023
ms.keywords: IWMDRMTranscryptor, IWMDRMTranscryptor interface [windows Media Format], IWMDRMTranscryptor interface [windows Media Format],described, IWMDRMTranscryptorInterface, wmformat.iwmdrmtranscryptor, wmsdkidl/IWMDRMTranscryptor
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
 - IWMDRMTranscryptor
 - wmsdkidl/IWMDRMTranscryptor
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
 - IWMDRMTranscryptor
---

# IWMDRMTranscryptor interface


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>IWMDRMTranscryptor</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>IWMDRMTranscryptor</b> interface transforms a DRM-protected ASF file into a secure data stream conforming to the Windows Media DRM 10 for Network Devices protocol. The resulting stream can be sent to devices that support Windows Media DRM 10 for Network Devices.

<b>IWMDRMTranscryptor</b> is the primary interface of the DRM transcryptor object. You can obtain a pointer to an instance of this interface by calling the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatedrmtranscryptor">WMCreateDRMTranscryptor</a> function.

## -inheritance

The <b>IWMDRMTranscryptor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWMDRMTranscryptor</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

The DRM transcryptor is initialized after a policy request message is sent by a device. You can parse a license request and obtain the device certificate, the device serial number, and the requested action by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdrmmessageparser-parselicenserequestmsg">IWMDRMMessageParser::ParseLicenseRequestMsg</a>.

The methods of the <b>IWMDRMTranscryptor</b> interface use the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus">IWMStatusCallback::OnStatus</a> callback method to inform the application of progress. For more information, see <a href="/windows/desktop/wmformat/using-the-callback-methods">Using the Callback Methods</a>.

## -see-also

<a href="/windows/desktop/wmformat/interfaces">Interfaces</a>
