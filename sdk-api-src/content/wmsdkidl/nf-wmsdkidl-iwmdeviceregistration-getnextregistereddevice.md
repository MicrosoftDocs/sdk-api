---
UID: NF:wmsdkidl.IWMDeviceRegistration.GetNextRegisteredDevice
title: IWMDeviceRegistration::GetNextRegisteredDevice (wmsdkidl.h)
description: The GetNextRegisteredDevice method enumerates the registered devices of a specified type.
helpviewer_keywords: ["GetNextRegisteredDevice","GetNextRegisteredDevice method [windows Media Format]","GetNextRegisteredDevice method [windows Media Format]","IWMDeviceRegistration interface","IWMDeviceRegistration interface [windows Media Format]","GetNextRegisteredDevice method","IWMDeviceRegistration.GetNextRegisteredDevice","IWMDeviceRegistration::GetNextRegisteredDevice","IWMDeviceRegistrationGetNextRegisteredDevice","wmformat.iwmdeviceregistration_getnextregistereddevice","wmsdkidl/IWMDeviceRegistration::GetNextRegisteredDevice"]
old-location: wmformat\iwmdeviceregistration_getnextregistereddevice.htm
tech.root: wmformat
ms.assetid: 396e60a8-5845-45fa-8393-6f0defbd38bb
ms.date: 4/26/2023
ms.keywords: GetNextRegisteredDevice, GetNextRegisteredDevice method [windows Media Format], GetNextRegisteredDevice method [windows Media Format],IWMDeviceRegistration interface, IWMDeviceRegistration interface [windows Media Format],GetNextRegisteredDevice method, IWMDeviceRegistration.GetNextRegisteredDevice, IWMDeviceRegistration::GetNextRegisteredDevice, IWMDeviceRegistrationGetNextRegisteredDevice, wmformat.iwmdeviceregistration_getnextregistereddevice, wmsdkidl/IWMDeviceRegistration::GetNextRegisteredDevice
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
 - IWMDeviceRegistration::GetNextRegisteredDevice
 - wmsdkidl/IWMDeviceRegistration::GetNextRegisteredDevice
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
 - IWMDeviceRegistration.GetNextRegisteredDevice
---

# IWMDeviceRegistration::GetNextRegisteredDevice


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<p class="CCE_Message">[<b>GetNextRegisteredDevice</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions. Instead, use <a href="https://www.microsoft.com/PlayReady/">Microsoft PlayReady</a>.
]


The <b>GetNextRegisteredDevice</b> method enumerates the registered devices of a specified type.

## -parameters

### -param ppDevice [out]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice</a> interface. This interface provides access to information about a registered device in the database that matches the type specified by the <i>dwRegisterType</i> parameter used in the call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice">GetFirstRegisteredDevice</a>. The information applies to the next device in the list (after the device retrieved previously).

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There are no more devices of the specified type in the list. When this value is returned, the address pointed to by <i>ppDevice</i> is set to <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppDevice</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

To enumerate registered devices of a given type, begin by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmdeviceregistration-getfirstregistereddevice">GetFirstRegisteredDevice</a> to retrieve the first device. Then make repeated calls to this method to get subsequent devices from the list. After all devices of the specified types have been retrieved, the next call to <b>GetNextRegisteredDevice</b> returns S_FALSE and the address pointed to by <i>ppDevice</i> is set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdeviceregistration">IWMDeviceRegistration Interface</a>