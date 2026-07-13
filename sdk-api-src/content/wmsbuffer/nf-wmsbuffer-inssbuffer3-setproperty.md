---
UID: NF:wmsbuffer.INSSBuffer3.SetProperty
title: INSSBuffer3::SetProperty (wmsbuffer.h)
description: The SetProperty method is used to specify a property for the sample in the buffer. Buffer properties are used to pass information along with the sample to the writer object when writing ASF files. Sample properties are GUID values.
helpviewer_keywords: ["INSSBuffer3 interface [windows Media Format]","SetProperty method","INSSBuffer3.SetProperty","INSSBuffer3::SetProperty","INSSBuffer3SetProperty","SetProperty","SetProperty method [windows Media Format]","SetProperty method [windows Media Format]","INSSBuffer3 interface","wmformat.inssbuffer3_setproperty","wmsbuffer/INSSBuffer3::SetProperty"]
old-location: wmformat\inssbuffer3_setproperty.htm
tech.root: wmformat
ms.assetid: 5aede025-65ae-4615-9511-af22b8c0dc00
ms.date: 4/26/2023
ms.keywords: INSSBuffer3 interface [windows Media Format],SetProperty method, INSSBuffer3.SetProperty, INSSBuffer3::SetProperty, INSSBuffer3SetProperty, SetProperty, SetProperty method [windows Media Format], SetProperty method [windows Media Format],INSSBuffer3 interface, wmformat.inssbuffer3_setproperty, wmsbuffer/INSSBuffer3::SetProperty
req.header: wmsbuffer.h
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
 - INSSBuffer3::SetProperty
 - wmsbuffer/INSSBuffer3::SetProperty
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
 - INSSBuffer3.SetProperty
---

# INSSBuffer3::SetProperty


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>SetProperty</b> method is used to specify a property for the sample in the buffer. Buffer properties are used to pass information along with the sample to the writer object when writing ASF files. Sample properties are GUID values.

## -parameters

### -param guidBufferProperty [in]

<b>GUID</b> value identifying the property you want to set. The predefined buffer properties are described in the <a href="/windows/desktop/wmformat/sample-extension-types">Sample Extension Types</a> section of this documentation. You can also define your own sample extension schemes using your own GUID values.

### -param pvBufferProperty [in]

Pointer to a buffer containing the property value.

### -param dwBufferPropertySize [in]

<b>DWORD</b> value containing the size of the buffer pointed to by <i>pvBufferProperty</i>.

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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to allocate memory for the new property.

</td>
</tr>
</table>

## -remarks

If you set a buffer property with a size larger than that specified in your call to <a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension">IWMStreamConfig2::AddDataUnitExtension</a>, you will not get an error from <b>SetProperty</b>. However, when the writer writes the sample, NS_E_DATA_UNIT_EXTENSION_TOO_LARGE will be returned.

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3 Interface</a>



<a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty">INSSBuffer3::GetProperty</a>