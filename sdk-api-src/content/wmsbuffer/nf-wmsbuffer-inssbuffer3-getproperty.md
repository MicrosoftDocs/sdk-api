---
UID: NF:wmsbuffer.INSSBuffer3.GetProperty
title: INSSBuffer3::GetProperty (wmsbuffer.h)
description: The GetProperty method is used to retrieve a property of the sample in the buffer. Buffer properties are used to pass information along with the sample to the writer object when writing ASF files. Sample properties are GUID values.
helpviewer_keywords: ["GetProperty","GetProperty method [windows Media Format]","GetProperty method [windows Media Format]","INSSBuffer3 interface","INSSBuffer3 interface [windows Media Format]","GetProperty method","INSSBuffer3.GetProperty","INSSBuffer3::GetProperty","INSSBuffer3GetProperty","wmformat.inssbuffer3_getproperty","wmsbuffer/INSSBuffer3::GetProperty"]
old-location: wmformat\inssbuffer3_getproperty.htm
tech.root: wmformat
ms.assetid: b7733df5-f764-4996-b324-fa050b1db0af
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [windows Media Format], GetProperty method [windows Media Format],INSSBuffer3 interface, INSSBuffer3 interface [windows Media Format],GetProperty method, INSSBuffer3.GetProperty, INSSBuffer3::GetProperty, INSSBuffer3GetProperty, wmformat.inssbuffer3_getproperty, wmsbuffer/INSSBuffer3::GetProperty
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
 - INSSBuffer3::GetProperty
 - wmsbuffer/INSSBuffer3::GetProperty
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
 - INSSBuffer3.GetProperty
---

# INSSBuffer3::GetProperty


## -description

The <b>GetProperty</b> method is used to retrieve a property of the sample in the buffer. Buffer properties are used to pass information along with the sample to the writer object when writing ASF files. Sample properties are GUID values.

## -parameters

### -param guidBufferProperty [in]

<b>GUID</b> value identifying the property to retrieve. The predefined buffer properties are described in the <a href="/windows/desktop/wmformat/sample-extension-types">Sample Extension Types</a> section of this documentation. You can also define your own sample extension schemes using your own GUID values.

### -param pvBufferProperty [out]

Pointer to a buffer that will receive the value of the property specified by <i>guidBufferProperty</i>.

### -param pdwBufferPropertySize [in, out]

Pointer to a <b>DWORD</b> value containing the size of the buffer pointed to by <i>pvBufferProperty</i>. If you pass <b>NULL</b> for <i>pvBufferProperty</i>, the method sets the value pointed to by this parameter to the size required to hold the property value. If you pass a non-<b>NULL</b> value for <i>pvBufferProperty</i>, the value pointed to by this parameter must equal the size of the buffer pointed to by <i>pvBufferProperty</i>.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pdwBufferPropertySize</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_UNSUPPORTED_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
The property specified as <i>guidBufferProperty</i> is not set in this buffer object.

</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer3">INSSBuffer3 Interface</a>



<a href="/previous-versions/windows/desktop/api/wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty">INSSBuffer3::SetProperty</a>