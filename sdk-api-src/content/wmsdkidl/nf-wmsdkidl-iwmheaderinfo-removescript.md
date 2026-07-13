---
UID: NF:wmsdkidl.IWMHeaderInfo.RemoveScript
title: IWMHeaderInfo::RemoveScript (wmsdkidl.h)
description: The RemoveScript method enables the object to remove a script from the header section of the ASF file.
helpviewer_keywords: ["IWMHeaderInfo interface [windows Media Format]","RemoveScript method","IWMHeaderInfo.RemoveScript","IWMHeaderInfo::RemoveScript","IWMHeaderInfoRemoveScript","RemoveScript","RemoveScript method [windows Media Format]","RemoveScript method [windows Media Format]","IWMHeaderInfo interface","wmformat.iwmheaderinfo_removescript","wmsdkidl/IWMHeaderInfo::RemoveScript"]
old-location: wmformat\iwmheaderinfo_removescript.htm
tech.root: wmformat
ms.assetid: c66e808d-25f9-4745-8bcc-731f2556f470
ms.date: 4/26/2023
ms.keywords: IWMHeaderInfo interface [windows Media Format],RemoveScript method, IWMHeaderInfo.RemoveScript, IWMHeaderInfo::RemoveScript, IWMHeaderInfoRemoveScript, RemoveScript, RemoveScript method [windows Media Format], RemoveScript method [windows Media Format],IWMHeaderInfo interface, wmformat.iwmheaderinfo_removescript, wmsdkidl/IWMHeaderInfo::RemoveScript
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
 - IWMHeaderInfo::RemoveScript
 - wmsdkidl/IWMHeaderInfo::RemoveScript
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
 - IWMHeaderInfo.RemoveScript
---

# IWMHeaderInfo::RemoveScript


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>RemoveScript</b> method enables the object to remove a script from the header section of the ASF file.

## -parameters

### -param wIndex [in]

<b>WORD</b> containing the index of the script.

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
<dt><b>NS_E_INVALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
The object cannot be currently configured.

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

The writer only supports this method before the <b>BeginWriting</b> method has been called. This method is not supported by the reader.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo">IWMHeaderInfo Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-addscript">IWMHeaderInfo::AddScript</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getscript">IWMHeaderInfo::GetScript</a>