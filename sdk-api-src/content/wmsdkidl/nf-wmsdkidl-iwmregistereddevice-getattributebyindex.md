---
UID: NF:wmsdkidl.IWMRegisteredDevice.GetAttributeByIndex
title: IWMRegisteredDevice::GetAttributeByIndex (wmsdkidl.h)
description: The GetAttributeByIndex method retrieves an attribute associated with the device. This method uses the attribute index to specify the attribute to retrieve.
helpviewer_keywords: ["GetAttributeByIndex","GetAttributeByIndex method [windows Media Format]","GetAttributeByIndex method [windows Media Format]","IWMRegisteredDevice interface","IWMRegisteredDevice interface [windows Media Format]","GetAttributeByIndex method","IWMRegisteredDevice.GetAttributeByIndex","IWMRegisteredDevice::GetAttributeByIndex","IWMRegisteredDeviceGetAttributeByIndex","wmformat.iwmregistereddevice_getattributebyindex","wmsdkidl/IWMRegisteredDevice::GetAttributeByIndex"]
old-location: wmformat\iwmregistereddevice_getattributebyindex.htm
tech.root: wmformat
ms.assetid: 02a582d4-329e-47e3-9dbe-dba8a3e4b4b3
ms.date: 4/26/2023
ms.keywords: GetAttributeByIndex, GetAttributeByIndex method [windows Media Format], GetAttributeByIndex method [windows Media Format],IWMRegisteredDevice interface, IWMRegisteredDevice interface [windows Media Format],GetAttributeByIndex method, IWMRegisteredDevice.GetAttributeByIndex, IWMRegisteredDevice::GetAttributeByIndex, IWMRegisteredDeviceGetAttributeByIndex, wmformat.iwmregistereddevice_getattributebyindex, wmsdkidl/IWMRegisteredDevice::GetAttributeByIndex
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
 - IWMRegisteredDevice::GetAttributeByIndex
 - wmsdkidl/IWMRegisteredDevice::GetAttributeByIndex
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
 - IWMRegisteredDevice.GetAttributeByIndex
---

# IWMRegisteredDevice::GetAttributeByIndex


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetAttributeByIndex</b> method retrieves an attribute associated with the device. This method uses the attribute index to specify the attribute to retrieve.

## -parameters

### -param dwIndex [in]

Attribute index. Valid indexes range from zero to one less than the number of attributes returned by <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-getattributecount">GetAttributeCount</a>.

### -param pbstrName [out]

Address of a variable that receives the attribute name.

### -param pbstrValue [out]

Address of a variable that receives the attribute value.

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