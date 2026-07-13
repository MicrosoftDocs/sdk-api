---
UID: NF:wmsdkidl.IWMHeaderInfo.GetScript
title: IWMHeaderInfo::GetScript (wmsdkidl.h)
description: The GetScript method returns the type and command strings, and the presentation time, of a script.
helpviewer_keywords: ["GetScript","GetScript method [windows Media Format]","GetScript method [windows Media Format]","IWMHeaderInfo interface","GetScript method [windows Media Format]","IWMHeaderInfo2 interface","GetScript method [windows Media Format]","IWMHeaderInfo3 interface","IWMHeaderInfo interface [windows Media Format]","GetScript method","IWMHeaderInfo.GetScript","IWMHeaderInfo2 interface [windows Media Format]","GetScript method","IWMHeaderInfo2::GetScript","IWMHeaderInfo3 interface [windows Media Format]","GetScript method","IWMHeaderInfo3::GetScript","IWMHeaderInfo::GetScript","IWMHeaderInfoGetScript","wmformat.iwmheaderinfo_getscript","wmsdkidl/IWMHeaderInfo2::GetScript","wmsdkidl/IWMHeaderInfo3::GetScript","wmsdkidl/IWMHeaderInfo::GetScript"]
old-location: wmformat\iwmheaderinfo_getscript.htm
tech.root: wmformat
ms.assetid: 779a7618-9f22-4caf-8a4e-b622e422c30d
ms.date: 4/26/2023
ms.keywords: GetScript, GetScript method [windows Media Format], GetScript method [windows Media Format],IWMHeaderInfo interface, GetScript method [windows Media Format],IWMHeaderInfo2 interface, GetScript method [windows Media Format],IWMHeaderInfo3 interface, IWMHeaderInfo interface [windows Media Format],GetScript method, IWMHeaderInfo.GetScript, IWMHeaderInfo2 interface [windows Media Format],GetScript method, IWMHeaderInfo2::GetScript, IWMHeaderInfo3 interface [windows Media Format],GetScript method, IWMHeaderInfo3::GetScript, IWMHeaderInfo::GetScript, IWMHeaderInfoGetScript, wmformat.iwmheaderinfo_getscript, wmsdkidl/IWMHeaderInfo2::GetScript, wmsdkidl/IWMHeaderInfo3::GetScript, wmsdkidl/IWMHeaderInfo::GetScript
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
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
 - IWMHeaderInfo::GetScript
 - wmsdkidl/IWMHeaderInfo::GetScript
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
 - qasf.dll
api_name:
 - IWMHeaderInfo.GetScript
 - IWMHeaderInfo2.GetScript
 - IWMHeaderInfo3.GetScript
---

# IWMHeaderInfo::GetScript


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>GetScript</b> method returns the type and command strings, and the presentation time, of a script.

## -parameters

### -param wIndex [in]

<b>WORD</b> that contains the index.

### -param pwszType [out]

Pointer to a wide-character <b>null</b>-terminated string buffer into which the type is copied.

### -param pcchTypeLen [in, out]

On input, a pointer to a variable that contains the length of the <i>pwszType</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the actual length of the string loaded into <i>pwszType</i>.This includes the terminating <b>null</b> character. To retrieve the length of the type, you must set this to zero and set <i>pwszType</i> to <b>NULL</b>.

### -param pwszCommand [out]

Pointer to a wide-character <b>null</b>-terminated string buffer into which the command is copied.

### -param pcchCommandLen [in, out]

On input, a pointer to a variable that contains the length of the <i>pwszCommand</i> array in wide characters (2 bytes). On output, if the method succeeds, the variable contains the actual length of the command string. This  includes the terminating <b>null</b> character. To retrieve the length of the command, you must set this to zero and set <i>pwszCommand</i> to <b>NULL</b>.

### -param pcnsScriptTime [out]

Pointer to a <b>QWORD</b> that specifies the presentation time of this script command in 100-nanosecond increments.

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
<dt><b>ASF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The size specified by <i>pcchCommandLen</i> or <i>pcchTypeLen</i> is not large enough to receive the value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
A script command that matches was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object is not in a configurable state.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A pointer is <b>NULL</b> where a value is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A pointer variable does not contain a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The method failed for an unspecified reason.

</td>
</tr>
</table>

## -remarks

You should make two calls to <b>GetScript</b> for each script you want to retrieve. On the first call, pass <b>NULL</b> for <i>pwszType</i> and <i>pwszCommand</i>. On return, the values that are pointed to by <i>pcchTypeLen</i> and <i>pcchCommandLen</i> are set to the number of wide characters. These  include the terminating <b>null</b> character, which is required to hold the script type in <i>pcchTypeLen</i> and the command in <i>pcchCommandLen</i>. You can then create buffers of the appropriate size to receive <i>pwszType</i> and <i>pwszCommand</i> and pass pointers to them on the second call.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo2">IWMHeaderInfo2</a>



<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3">IWMHeaderInfo3</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript">IWMHeaderInfo::AddScript</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscriptcount">IWMHeaderInfo::GetScriptCount</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-removescript">IWMHeaderInfo::RemoveScript</a>