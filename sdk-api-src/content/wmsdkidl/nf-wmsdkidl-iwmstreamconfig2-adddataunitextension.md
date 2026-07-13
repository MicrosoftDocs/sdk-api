---
UID: NF:wmsdkidl.IWMStreamConfig2.AddDataUnitExtension
title: IWMStreamConfig2::AddDataUnitExtension (wmsdkidl.h)
description: The AddDataUnitExtension method adds a data unit extension system to the stream. You can use data unit extension systems to attach custom data to samples in an output file.
helpviewer_keywords: ["AddDataUnitExtension","AddDataUnitExtension method [windows Media Format]","AddDataUnitExtension method [windows Media Format]","IWMStreamConfig2 interface","IWMStreamConfig2 interface [windows Media Format]","AddDataUnitExtension method","IWMStreamConfig2.AddDataUnitExtension","IWMStreamConfig2::AddDataUnitExtension","IWMStreamConfig2AddDataUnitExtension","wmformat.iwmstreamconfig2_adddataunitextension","wmsdkidl/IWMStreamConfig2::AddDataUnitExtension"]
old-location: wmformat\iwmstreamconfig2_adddataunitextension.htm
tech.root: wmformat
ms.assetid: db84a33c-bd83-46cb-a97c-76ddeeb74927
ms.date: 4/26/2023
ms.keywords: AddDataUnitExtension, AddDataUnitExtension method [windows Media Format], AddDataUnitExtension method [windows Media Format],IWMStreamConfig2 interface, IWMStreamConfig2 interface [windows Media Format],AddDataUnitExtension method, IWMStreamConfig2.AddDataUnitExtension, IWMStreamConfig2::AddDataUnitExtension, IWMStreamConfig2AddDataUnitExtension, wmformat.iwmstreamconfig2_adddataunitextension, wmsdkidl/IWMStreamConfig2::AddDataUnitExtension
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMStreamConfig2::AddDataUnitExtension
 - wmsdkidl/IWMStreamConfig2::AddDataUnitExtension
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmvcore.lib
 - Wmvcore.dll
 - WMStubDRM.lib
 - WMStubDRM.dll
api_name:
 - IWMStreamConfig2.AddDataUnitExtension
---

# IWMStreamConfig2::AddDataUnitExtension


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AddDataUnitExtension</b> method adds a data unit extension system to the stream. You can use data unit extension systems to attach custom data to samples in an output file.

## -parameters

### -param guidExtensionSystemID [in]

A GUID that identifies the data unit extension system. This can be one of the predefined GUIDs listed in <a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty">INSSBuffer3::SetProperty</a>, or a GUID whose value is understood by a custom player application.

### -param cbExtensionDataSize [in]

Size, in bytes, of the data unit extensions that will be attached to the packets in the stream. Set to 0xFFFF to specify data unit extensions of variable size. Each individual data unit extension can then be set to any size ranging from 0 to 65534.

### -param pbExtensionSystemInfo [in]

Pointer to a byte buffer containing information about the data unit extension system. If you have no information, you can pass <b>NULL</b>. When passing <b>NULL</b>, <i>cbExtensionSystemInfo</i> must be zero.

### -param cbExtensionSystemInfo [in]

Count of bytes in the buffer at <i>pbExtensionSystemInfo</i>. If you have no data unit extension system information, you can pass zero. When passing zero, <i>pbExtensionSystemInfo</i> must be <b>NULL</b>.

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
<i>cbExtensionSystemInfo</i> specifies a non-zero value, but <i>pbExtensionSystemInfo</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method cannot allocate memory to hold the new data unit extension.

</td>
</tr>
</table>

## -remarks

Passing the GUID of an existing data unit extension system does not cause an error. The old system is destroyed and replaced by the new one.

The new value will not take effect in the profile until you call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream">IWMProfile::ReconfigStream</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension">IWMStreamConfig2::GetDataUnitExtension</a>