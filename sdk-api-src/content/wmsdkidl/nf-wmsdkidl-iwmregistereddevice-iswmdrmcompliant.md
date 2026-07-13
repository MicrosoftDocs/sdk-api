---
UID: NF:wmsdkidl.IWMRegisteredDevice.IsWmdrmCompliant
title: IWMRegisteredDevice::IsWmdrmCompliant (wmsdkidl.h)
description: The IsWmdrmCompliant method retrieves the DRM compliance status of the device. Compliant devices can receive data using the Windows Media DRM 10 for Network Devices protocol.
helpviewer_keywords: ["IWMRegisteredDevice interface [windows Media Format]","IsWmdrmCompliant method","IWMRegisteredDevice.IsWmdrmCompliant","IWMRegisteredDevice::IsWmdrmCompliant","IWMRegisteredDeviceIsWmdrmCompliant","IsWmdrmCompliant","IsWmdrmCompliant method [windows Media Format]","IsWmdrmCompliant method [windows Media Format]","IWMRegisteredDevice interface","wmformat.iwmregistereddevice_iswmdrmcompliant","wmsdkidl/IWMRegisteredDevice::IsWmdrmCompliant"]
old-location: wmformat\iwmregistereddevice_iswmdrmcompliant.htm
tech.root: wmformat
ms.assetid: 45bc7abb-1d39-4988-a9f0-867eaefe148f
ms.date: 4/26/2023
ms.keywords: IWMRegisteredDevice interface [windows Media Format],IsWmdrmCompliant method, IWMRegisteredDevice.IsWmdrmCompliant, IWMRegisteredDevice::IsWmdrmCompliant, IWMRegisteredDeviceIsWmdrmCompliant, IsWmdrmCompliant, IsWmdrmCompliant method [windows Media Format], IsWmdrmCompliant method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_iswmdrmcompliant, wmsdkidl/IWMRegisteredDevice::IsWmdrmCompliant
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
 - IWMRegisteredDevice::IsWmdrmCompliant
 - wmsdkidl/IWMRegisteredDevice::IsWmdrmCompliant
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
 - IWMRegisteredDevice.IsWmdrmCompliant
---

# IWMRegisteredDevice::IsWmdrmCompliant


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>IsWmdrmCompliant</b> method retrieves the DRM compliance status of the device. Compliant devices can receive data using the Windows Media DRM 10 for Network Devices protocol.

## -parameters

### -param pfCompliant [out]

Address of a variable that receives the device DRM compliance status. <b>TRUE</b> indicates that Windows Media DRM 10 for Network Devices is supported.

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

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice Interface</a>