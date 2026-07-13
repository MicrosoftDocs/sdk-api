---
UID: NF:wmsdkidl.IWMRegisteredDevice.IsValid
title: IWMRegisteredDevice::IsValid (wmsdkidl.h)
description: The IsValid method retrieves the validation status of the device.
helpviewer_keywords: ["IWMRegisteredDevice interface [windows Media Format]","IsValid method","IWMRegisteredDevice.IsValid","IWMRegisteredDevice::IsValid","IWMRegisteredDeviceIsValid","IsValid","IsValid method [windows Media Format]","IsValid method [windows Media Format]","IWMRegisteredDevice interface","wmformat.iwmregistereddevice_isvalid","wmsdkidl/IWMRegisteredDevice::IsValid"]
old-location: wmformat\iwmregistereddevice_isvalid.htm
tech.root: wmformat
ms.assetid: ce09e6ad-10c0-4cdd-8dee-4faacd958f2b
ms.date: 4/26/2023
ms.keywords: IWMRegisteredDevice interface [windows Media Format],IsValid method, IWMRegisteredDevice.IsValid, IWMRegisteredDevice::IsValid, IWMRegisteredDeviceIsValid, IsValid, IsValid method [windows Media Format], IsValid method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_isvalid, wmsdkidl/IWMRegisteredDevice::IsValid
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
 - IWMRegisteredDevice::IsValid
 - wmsdkidl/IWMRegisteredDevice::IsValid
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
 - IWMRegisteredDevice.IsValid
---

# IWMRegisteredDevice::IsValid


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IsValid</b> method retrieves the validation status of the device.

## -parameters

### -param pfValid [out]

Address of a variable that receives the validation status of the device. <b>TRUE</b> indicates that the device is valid. <b>FALSE</b> indicates that the device is not valid and needs to be revalidated before it can be used.

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

You can find out whether the device is open by calling <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isopened">IsOpened</a>. To open the device call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-open">Open</a>.

A device is validated by performing proximity detection. For more information, see the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmproximitydetection">IWMProximityDetection</a> interface.

Call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-isapproved">IsApproved</a> method to determine whether the device is approved. To approve the device, call the <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-approve">Approve</a> method.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice Interface</a>