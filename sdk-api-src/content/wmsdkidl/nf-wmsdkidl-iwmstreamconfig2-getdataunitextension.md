---
UID: NF:wmsdkidl.IWMStreamConfig2.GetDataUnitExtension
title: IWMStreamConfig2::GetDataUnitExtension (wmsdkidl.h)
description: The GetDataUnitExtension method retrieves information about an existing data unit extension system.
helpviewer_keywords: ["GetDataUnitExtension","GetDataUnitExtension method [windows Media Format]","GetDataUnitExtension method [windows Media Format]","IWMStreamConfig2 interface","IWMStreamConfig2 interface [windows Media Format]","GetDataUnitExtension method","IWMStreamConfig2.GetDataUnitExtension","IWMStreamConfig2::GetDataUnitExtension","IWMStreamConfig2GetDataUnitExtension","wmformat.iwmstreamconfig2_getdataunitextension","wmsdkidl/IWMStreamConfig2::GetDataUnitExtension"]
old-location: wmformat\iwmstreamconfig2_getdataunitextension.htm
tech.root: wmformat
ms.assetid: 766124f6-b376-421b-b2ee-2c280af3bd16
ms.date: 4/26/2023
ms.keywords: GetDataUnitExtension, GetDataUnitExtension method [windows Media Format], GetDataUnitExtension method [windows Media Format],IWMStreamConfig2 interface, IWMStreamConfig2 interface [windows Media Format],GetDataUnitExtension method, IWMStreamConfig2.GetDataUnitExtension, IWMStreamConfig2::GetDataUnitExtension, IWMStreamConfig2GetDataUnitExtension, wmformat.iwmstreamconfig2_getdataunitextension, wmsdkidl/IWMStreamConfig2::GetDataUnitExtension
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
 - IWMStreamConfig2::GetDataUnitExtension
 - wmsdkidl/IWMStreamConfig2::GetDataUnitExtension
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
 - IWMStreamConfig2.GetDataUnitExtension
---

# IWMStreamConfig2::GetDataUnitExtension


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDataUnitExtension</b> method retrieves information about an existing data unit extension system.

## -parameters

### -param wDataUnitExtensionNumber [in]

<b>WORD</b> containing the data unit extension number. This number is assigned to a data unit extension system when it is added to the stream.

### -param pguidExtensionSystemID [out]

Pointer to a GUID that receives the identifier of the data unit extension system.

### -param pcbExtensionDataSize [out]

Pointer to the size, in bytes, of the data unit extensions that will be attached to the packets in the stream.

If this value is 0xFFFF, the system uses data unit extensions of variable size. Each individual data unit extension can then be set to any size ranging from 0 to 65534.

### -param pbExtensionSystemInfo [out]

Pointer to a byte buffer that receives information about the data unit extension system.

### -param pcbExtensionSystemInfo [in, out]

Pointer to the size, in bytes, of the data stored at <i>pbExtensionSystemInfo</i>.

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
<i>pguidExtensionSystemID</i> or <i>pcbExtensionDataSize</i> is <b>NULL</b>.

OR

<i>wDataUnitExtensionNumber</i> specifies an invalid data unit extension number.

</td>
</tr>
</table>

## -remarks

To retrieve the total number of data unit extension systems associated with the stream, call <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount">GetDataUnitExtensionCount</a>.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension">IWMStreamConfig2::AddDataUnitExtension</a>