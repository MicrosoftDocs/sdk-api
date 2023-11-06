---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetAttributeCount
title: IWMRegisteredDevice::GetAttributeCount (wmsdkidl.h)
description: The GetAttributeCount method retrieves the total number of attributes associated with the device.
helpviewer_keywords: ["GetAttributeCount","GetAttributeCount method [windows Media Format]","GetAttributeCount method [windows Media Format]","IWMRegisteredDevice interface","IWMRegisteredDevice interface [windows Media Format]","GetAttributeCount method","IWMRegisteredDevice.GetAttributeCount","IWMRegisteredDevice::GetAttributeCount","IWMRegisteredDeviceGetAttributeCount","wmformat.iwmregistereddevice_getattributecount","wmsdkidl/IWMRegisteredDevice::GetAttributeCount"]
old-location: wmformat\iwmregistereddevice_getattributecount.htm
tech.root: wmformat
ms.assetid: 6032cb18-4c4a-4cd7-905e-5cb390bfc37b
ms.date: 4/26/2023
ms.keywords: GetAttributeCount, GetAttributeCount method [windows Media Format], GetAttributeCount method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetAttributeCount method, IWMRegisteredDevice.GetAttributeCount, IWMRegisteredDevice::GetAttributeCount, IWMRegisteredDeviceGetAttributeCount, wmformat.iwmregistereddevice_getattributecount, wmsdkidl/IWMRegisteredDevice::GetAttributeCount
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
 - IWMRegisteredDevice::GetAttributeCount
 - wmsdkidl/IWMRegisteredDevice::GetAttributeCount
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
 - IWMRegisteredDevice.GetAttributeCount
---

# IWMRegisteredDevice::GetAttributeCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAttributeCount</b> method retrieves the total number of attributes associated with the device.

## -parameters

### -param pcAttributes [out]

Address of a variable that receives the number of attributes.

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

To enumerate the device attributes, first call this method and then call <a href="/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-getattributebyindex">GetAttributeByIndex</a> for index values from zero through one less than the total number of attributes.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistereddevice">IWMRegisteredDevice Interface</a>