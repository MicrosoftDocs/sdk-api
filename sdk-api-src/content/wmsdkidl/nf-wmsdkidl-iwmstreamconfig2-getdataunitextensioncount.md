---
UID: NF:wmsdkidl.IWMStreamConfig2.GetDataUnitExtensionCount
title: IWMStreamConfig2::GetDataUnitExtensionCount (wmsdkidl.h)
description: The GetDataUnitExtensionCount method retrieves the total number of data unit extension systems that have been added to the stream.
helpviewer_keywords: ["GetDataUnitExtensionCount","GetDataUnitExtensionCount method [windows Media Format]","GetDataUnitExtensionCount method [windows Media Format]","IWMStreamConfig2 interface","IWMStreamConfig2 interface [windows Media Format]","GetDataUnitExtensionCount method","IWMStreamConfig2.GetDataUnitExtensionCount","IWMStreamConfig2::GetDataUnitExtensionCount","IWMStreamConfig2GetDataUnitExtensionCount","wmformat.iwmstreamconfig2_getdataunitextensioncount","wmsdkidl/IWMStreamConfig2::GetDataUnitExtensionCount"]
old-location: wmformat\iwmstreamconfig2_getdataunitextensioncount.htm
tech.root: wmformat
ms.assetid: f9a4ec84-4ea3-4e84-9def-7ca93be0f1ce
ms.date: 4/26/2023
ms.keywords: GetDataUnitExtensionCount, GetDataUnitExtensionCount method [windows Media Format], GetDataUnitExtensionCount method [windows Media Format],IWMStreamConfig2 interface, IWMStreamConfig2 interface [windows Media Format],GetDataUnitExtensionCount method, IWMStreamConfig2.GetDataUnitExtensionCount, IWMStreamConfig2::GetDataUnitExtensionCount, IWMStreamConfig2GetDataUnitExtensionCount, wmformat.iwmstreamconfig2_getdataunitextensioncount, wmsdkidl/IWMStreamConfig2::GetDataUnitExtensionCount
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
 - IWMStreamConfig2::GetDataUnitExtensionCount
 - wmsdkidl/IWMStreamConfig2::GetDataUnitExtensionCount
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
 - IWMStreamConfig2.GetDataUnitExtensionCount
---

# IWMStreamConfig2::GetDataUnitExtensionCount


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetDataUnitExtensionCount</b> method retrieves the total number of data unit extension systems that have been added to the stream.

## -parameters

### -param pcDataUnitExtensions [out]

Pointer to a <b>WORD</b> that receives the count of data unit extensions.

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
<i>pcDataUnitExtensions</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2">IWMStreamConfig2 Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension">IWMStreamConfig2::GetDataUnitExtension</a>