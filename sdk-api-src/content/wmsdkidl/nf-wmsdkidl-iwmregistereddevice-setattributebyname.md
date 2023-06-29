---
UID: NF:wmsdkidl.IWMRegisteredDevice.SetAttributeByName
title: IWMRegisteredDevice::SetAttributeByName (wmsdkidl.h)
description: The SetAttributeByName method sets a device attribute.
helpviewer_keywords: ["IWMRegisteredDevice interface [windows Media Format]","SetAttributeByName method","IWMRegisteredDevice.SetAttributeByName","IWMRegisteredDevice::SetAttributeByName","IWMRegisteredDeviceSetAttributeByName","SetAttributeByName","SetAttributeByName method [windows Media Format]","SetAttributeByName method [windows Media Format]","IWMRegisteredDevice interface","wmformat.iwmregistereddevice_setattributebyname","wmsdkidl/IWMRegisteredDevice::SetAttributeByName"]
old-location: wmformat\iwmregistereddevice_setattributebyname.htm
tech.root: wmformat
ms.assetid: 49562f2a-1bb5-46d7-81cc-c13b66cf691f
ms.date: 4/26/2023
ms.keywords: IWMRegisteredDevice interface [windows Media Format],SetAttributeByName method, IWMRegisteredDevice.SetAttributeByName, IWMRegisteredDevice::SetAttributeByName, IWMRegisteredDeviceSetAttributeByName, SetAttributeByName, SetAttributeByName method [windows Media Format], SetAttributeByName method [windows Media Format],IWMRegisteredDevice interface, wmformat.iwmregistereddevice_setattributebyname, wmsdkidl/IWMRegisteredDevice::SetAttributeByName
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
 - IWMRegisteredDevice::SetAttributeByName
 - wmsdkidl/IWMRegisteredDevice::SetAttributeByName
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
 - IWMRegisteredDevice.SetAttributeByName
---

# IWMRegisteredDevice::SetAttributeByName


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetAttributeByName</b> method sets a device attribute.

## -parameters

### -param bstrName [in]

Name of the attribute to set.

### -param bstrValue [in]

Value of the attribute.

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



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmregistereddevice-getattributebyname">IWMRegisteredDevice::GetAttributeByName</a>