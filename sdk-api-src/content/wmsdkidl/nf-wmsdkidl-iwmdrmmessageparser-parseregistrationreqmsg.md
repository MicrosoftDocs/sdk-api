---
UID: NF:wmsdkidl.IWMDRMMessageParser.ParseRegistrationReqMsg
title: IWMDRMMessageParser::ParseRegistrationReqMsg (wmsdkidl.h)
description: The ParseRegistrationReqMsg method extracts the device certificate and identifier from a registration message sent by a device.
helpviewer_keywords: ["IWMDRMMessageParser interface [windows Media Format]","ParseRegistrationReqMsg method","IWMDRMMessageParser.ParseRegistrationReqMsg","IWMDRMMessageParser::ParseRegistrationReqMsg","IWMDRMMessageParserParseRegistrationReqMsg","ParseRegistrationReqMsg","ParseRegistrationReqMsg method [windows Media Format]","ParseRegistrationReqMsg method [windows Media Format]","IWMDRMMessageParser interface","wmformat.iwmdrmmessageparser_parseregistrationreqmsg","wmsdkidl/IWMDRMMessageParser::ParseRegistrationReqMsg"]
old-location: wmformat\iwmdrmmessageparser_parseregistrationreqmsg.htm
tech.root: wmformat
ms.assetid: d2d142bf-0fed-42c8-a2f1-b539a40ac074
ms.date: 4/26/2023
ms.keywords: IWMDRMMessageParser interface [windows Media Format],ParseRegistrationReqMsg method, IWMDRMMessageParser.ParseRegistrationReqMsg, IWMDRMMessageParser::ParseRegistrationReqMsg, IWMDRMMessageParserParseRegistrationReqMsg, ParseRegistrationReqMsg, ParseRegistrationReqMsg method [windows Media Format], ParseRegistrationReqMsg method [windows Media Format],IWMDRMMessageParser interface, wmformat.iwmdrmmessageparser_parseregistrationreqmsg, wmsdkidl/IWMDRMMessageParser::ParseRegistrationReqMsg
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
 - IWMDRMMessageParser::ParseRegistrationReqMsg
 - wmsdkidl/IWMDRMMessageParser::ParseRegistrationReqMsg
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
 - IWMDRMMessageParser.ParseRegistrationReqMsg
---

# IWMDRMMessageParser::ParseRegistrationReqMsg


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>ParseRegistrationReqMsg</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>ParseRegistrationReqMsg</b> method extracts the device certificate and identifier from a registration message sent by a device.

## -parameters

### -param pbRegistrationReqMsg [in]

Address of the registration message in memory. This is a message received by your application from a device.

### -param cbRegistrationReqMsg [in]

The size of registration message in bytes.

### -param ppDeviceCert [out]

Address of a variable that receives the address of the <a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface of the buffer object that contains the device certificate.

### -param pDeviceSerialNumber [out]

Address of a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-drm_val16">DRM_VAL16</a> structure that receives the device identifier.

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
The <i>pbRegistrationMsg</i> parameter is <b>NULL</b>, or the <i>cbRegistrationMsg</i> parameter is 0.

</td>
</tr>
</table>

## -remarks

Registration request messages are sent by devices when they are connected to a network shared by the computer running your application. When your application receives the message, it must first parse the message by using this method to retrieve the device certificate and device identifier. The combination of device certificate and device identifier uniquely identifies the device.

After parsing the message with this method, you can search the device database to determine whether the device is already registered, or you can try to register the device. Both of these actions use the methods of the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration</a> interface.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmmessageparser">IWMDRMMessageParser Interface</a>