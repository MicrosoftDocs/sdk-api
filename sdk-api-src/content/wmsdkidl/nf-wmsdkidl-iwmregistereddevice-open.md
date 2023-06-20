---
UID: NF:wmsdkidl.IWMRegisteredDevice.Open
title: IWMRegisteredDevice::Open (wmsdkidl.h)
description: The Open method opens the device so that it can receive media data.
helpviewer_keywords: ["IWMRegisteredDevice interface [windows Media Format]","Open method","IWMRegisteredDevice.Open","IWMRegisteredDevice::Open","IWMRegisteredDeviceOpen","Open","Open method [windows Media Format]","Open method [windows Media Format]","IWMRegisteredDevice interface","wmformat.iwmregistereddevice_open","wmsdkidl/IWMRegisteredDevice::Open"]
old-location: wmformat\iwmregistereddevice_open.htm
tech.root: wmformat
ms.assetid: 277f2724-5d82-4db7-96d9-af392b39fccf
ms.date: 4/26/2023
ms.keywords: IWMRegisteredDevice interface [windows Media Format],Open method, IWMRegisteredDevice.Open, IWMRegisteredDevice::Open, IWMRegisteredDeviceOpen, Open, Open method [windows Media Format], Open method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_open, wmsdkidl/IWMRegisteredDevice::Open
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
 - IWMRegisteredDevice::Open
 - wmsdkidl/IWMRegisteredDevice::Open
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
 - IWMRegisteredDevice.Open
---

# IWMRegisteredDevice::Open


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>Open</b> method opens the device so that it can receive media data.



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
<dt><b>NS_E_DRM_DEVICE_LIMIT_REACHED</b></dt>
</dl>
</td>
<td width="60%">
The client computer already has the maximum number of devices opened.

</td>
</tr>
</table>

## -remarks

To receive data, a device must be opened, validated, and approved.

Use this method to open the device. To determine whether the device is already open, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened">IsOpened</a>. Only 10 devices can be open on a computer at a time.

The device is valid only if proximity detection has been performed on it within the past 48 hours. You can check the validity of the device by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isvalid">IsValid</a>. For more information, see the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection">IWMProximityDetection</a> interface.

Call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved">IsApproved</a> method to determine whether the device is approved. To approve the device, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve">Approve</a> method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-close">IWMRegisteredDevice::Close</a>
