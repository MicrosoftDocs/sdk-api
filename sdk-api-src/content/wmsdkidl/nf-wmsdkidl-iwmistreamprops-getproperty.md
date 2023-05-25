---
UID: NF:wmsdkidl.IWMIStreamProps.GetProperty
title: IWMIStreamProps::GetProperty (wmsdkidl.h)
description: The GetProperty method retrieves a named property from the IStream.
helpviewer_keywords: ["GetProperty","GetProperty method [windows Media Format]","GetProperty method [windows Media Format]","IWMIStreamProps interface","IWMIStreamProps interface [windows Media Format]","GetProperty method","IWMIStreamProps.GetProperty","IWMIStreamProps::GetProperty","IWMIStreamPropsGetProperty","wmformat.iwmistreamprops_getproperty","wmsdkidl/IWMIStreamProps::GetProperty"]
old-location: wmformat\iwmistreamprops_getproperty.htm
tech.root: wmformat
ms.assetid: 1873e20f-376a-45fe-ad02-0c28c894af18
ms.date: 4/26/2023
ms.keywords: GetProperty, GetProperty method [windows Media Format], GetProperty method [windows Media Format],IWMIStreamProps interface, IWMIStreamProps interface [windows Media Format],GetProperty method, IWMIStreamProps.GetProperty, IWMIStreamProps::GetProperty, IWMIStreamPropsGetProperty, wmformat.iwmistreamprops_getproperty, wmsdkidl/IWMIStreamProps::GetProperty
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
 - IWMIStreamProps::GetProperty
 - wmsdkidl/IWMIStreamProps::GetProperty
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
 - IWMIStreamProps.GetProperty
---

# IWMIStreamProps::GetProperty


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetProperty</b> method retrieves a named property from the <b>IStream</b>.

## -parameters

### -param pszName [in]

Pointer to a <b>null</b>-terminated string containing the name of the property to retrieve. You should use the global identifier to refer to properties so that any error will appear at compile time. The following table lists the available <b>IStream</b> properties.

<table>
<tr>
<th>Property name
                </th>
<th>Global identifier
                </th>
</tr>
<tr>
<td><b>ReloadIndexOnSeek</b></td>
<td>g_wszReloadIndexOnSeek</td>
</tr>
<tr>
<td><b>StreamNumIndexObjects</b></td>
<td>g_wszStreamNumIndexObjects</td>
</tr>
<tr>
<td><b>FailSeekOnError</b></td>
<td>g_wszFailSeekOnError</td>
</tr>
<tr>
<td><b>PermitSeeksBeyondEndOfStream</b></td>
<td>g_wszPermitSeeksBeyondEndOfStream</td>
</tr>
<tr>
<td><b>UsePacketAtSeekPoint</b></td>
<td>g_wszUsePacketAtSeekPoint</td>
</tr>
<tr>
<td><b>SourceBufferTime</b></td>
<td>g_wszSourceBufferTime</td>
</tr>
<tr>
<td><b>SourceMaxBytesAtOnce</b></td>
<td>g_wszSourceMaxBytesAtOnce</td>
</tr>
</table>

### -param pType [out]

Pointer to a variable that will receive one member of the <a href="/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_attr_datatype">WMT_ATTR_DATATYPE</a> enumeration type. This value indicates the type of data in the buffer at <i>pValue</i>.

### -param pValue [out]

Pointer to a byte buffer that will receive the property value. The type of data returned to the buffer is indicated by the value pointed to by <i>pType</i>.

### -param pdwSize [in, out]

Pointer to a <b>DWORD</b> containing the size of the buffer at <i>pValue</i>. On return, this value will be set to the correct size of the property value.

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
<i>pType</i>, <i>pValue</i>, or <i>pdwSize</i> is <b>NULL</b>.

OR

The buffer is not big enough to hold the requested value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
<i>pszName</i> specifies an invalid property name.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetProperty</b> for each property you want to retrieve. On the first call, pass <b>NULL</b> as <i>pValue</i>. On return, the value pointed to by <i>pdwSize</i> will be set to the buffer size required to hold the property value. Then you can allocate the required amount of memory for the buffer and pass a pointer to it as <i>pValue</i> on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmistreamprops">IWMIStreamProps Interface</a>