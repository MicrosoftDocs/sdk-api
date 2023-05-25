---
UID: NF:wmsdkidl.IWMRegisteredDevice.IsOpened
title: IWMRegisteredDevice::IsOpened (wmsdkidl.h)
description: The IsOpened method retrieves the open status of the device. An open device is ready to receive media data.
helpviewer_keywords: ["IWMRegisteredDevice interface [windows Media Format]","IsOpened method","IWMRegisteredDevice.IsOpened","IWMRegisteredDevice::IsOpened","IWMRegisteredDeviceIsOpened","IsOpened","IsOpened method [windows Media Format]","IsOpened method [windows Media Format]","IWMRegisteredDevice interface","wmformat.iwmregistereddevice_isopened","wmsdkidl/IWMRegisteredDevice::IsOpened"]
old-location: wmformat\iwmregistereddevice_isopened.htm
tech.root: wmformat
ms.assetid: 5a8a6b2a-6a04-4505-b4be-ec10e1e5effe
ms.date: 4/26/2023
ms.keywords: IWMRegisteredDevice interface [windows Media Format],IsOpened method, IWMRegisteredDevice.IsOpened, IWMRegisteredDevice::IsOpened, IWMRegisteredDeviceIsOpened, IsOpened, IsOpened method [windows Media Format], IsOpened method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_isopened, wmsdkidl/IWMRegisteredDevice::IsOpened
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
 - IWMRegisteredDevice::IsOpened
 - wmsdkidl/IWMRegisteredDevice::IsOpened
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
 - IWMRegisteredDevice.IsOpened
---

# IWMRegisteredDevice::IsOpened


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IsOpened</b> method retrieves the open status of the device. An open device is ready to receive media data.

## -parameters

### -param pfOpened [out]

Address of a variable that receives the open status of the device. <b>TRUE</b> indicates that the device is open.

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
</table>

## -remarks

To receive data, a device must be opened, validated, and approved.

You can use this method to find out whether the device is open. To open the device call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open">Open</a>.

The device is valid only if proximity detection has been performed on it within the past 48 hours. You can check the validity of the device by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid">IsValid</a>. For more information, see the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection">IWMProximityDetection</a> interface.

Call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved">IsApproved</a> method to determine whether the device is approved. To approve the device, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve">Approve</a> method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice Interface</a>