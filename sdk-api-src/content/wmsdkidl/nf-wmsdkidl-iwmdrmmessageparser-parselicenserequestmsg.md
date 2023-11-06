---
UID: NF:wmsdkidl.IWMDRMMessageParser.ParseLicenseRequestMsg
title: IWMDRMMessageParser::ParseLicenseRequestMsg (wmsdkidl.h)
description: The ParseLicenseRequestMsg method extracts the device identification and requested action from a policy request message.
helpviewer_keywords: ["IWMDRMMessageParser interface [windows Media Format]","ParseLicenseRequestMsg method","IWMDRMMessageParser.ParseLicenseRequestMsg","IWMDRMMessageParser::ParseLicenseRequestMsg","IWMDRMMessageParserParseLicenseRequestMsg","ParseLicenseRequestMsg","ParseLicenseRequestMsg method [windows Media Format]","ParseLicenseRequestMsg method [windows Media Format]","IWMDRMMessageParser interface","wmformat.iwmdrmmessageparser_parselicenserequestmsg","wmsdkidl/IWMDRMMessageParser::ParseLicenseRequestMsg"]
old-location: wmformat\iwmdrmmessageparser_parselicenserequestmsg.htm
tech.root: wmformat
ms.assetid: 0d51b7f7-5cc2-4dbd-8a61-2901c01734bb
ms.date: 4/26/2023
ms.keywords: IWMDRMMessageParser interface [windows Media Format],ParseLicenseRequestMsg method, IWMDRMMessageParser.ParseLicenseRequestMsg, IWMDRMMessageParser::ParseLicenseRequestMsg, IWMDRMMessageParserParseLicenseRequestMsg, ParseLicenseRequestMsg, ParseLicenseRequestMsg method [windows Media Format], ParseLicenseRequestMsg method [windows Media Format],IWMDRMMessageParser interface, wmformat.iwmdrmmessageparser_parselicenserequestmsg, wmsdkidl/IWMDRMMessageParser::ParseLicenseRequestMsg
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only],Windows Media Format 9.5 SDK
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
req.lib: WMStubDRM.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMDRMMessageParser::ParseLicenseRequestMsg
 - wmsdkidl/IWMDRMMessageParser::ParseLicenseRequestMsg
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMDRMMessageParser.ParseLicenseRequestMsg
---

# IWMDRMMessageParser::ParseLicenseRequestMsg


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>ParseLicenseRequestMsg</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>ParseLicenseRequestMsg</b> method extracts the device identification and requested action from a policy request message.

## -parameters

### -param pbLicenseRequestMsg [in]

Address of the license request message in memory. This is a message received by your application from a device.

### -param cbLicenseRequestMsg [in]

The size of license request message in bytes.

### -param ppDeviceCert [out]

Address of a variable that receives the address of the <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface of the buffer object that contains the device certificate.

### -param pDeviceSerialNumber [out]

Address of a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_val16">DRM_VAL16</a> structure that receives the device identifier.

### -param pbstrAction [out]

Address of a variable that receives the string containing the requested action. The supported actions correspond to rights associates with DRM licenses. The only action string currently supported is "Play".

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pbLicenseRequestMsg</i> parameter is <b>NULL</b>, or the <i>cbLicenseRequestMsg</i> parameter is 0.

</td>
</tr>
</table>

## -remarks

The license request message sent by the device determines the action that your application should take. After parsing a message with the "Play" action, you can begin processing the file with the methods of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor">IWMDRMTranscryptor</a> interface.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser">IWMDRMMessageParser Interface</a>