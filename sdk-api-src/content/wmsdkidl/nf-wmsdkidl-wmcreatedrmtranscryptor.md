---
UID: NF:wmsdkidl.WMCreateDRMTranscryptor
title: WMCreateDRMTranscryptor function (wmsdkidl.h)
description: Creates a DRM transcryptor object.
helpviewer_keywords: ["WMCreateDRMTranscryptor","WMCreateDRMTranscryptor function [windows Media Format]","wmformat.wmcreatedrmtranscryptor","wmsdkidl/WMCreateDRMTranscryptor"]
old-location: wmformat\wmcreatedrmtranscryptor.htm
tech.root: wmformat
ms.assetid: b8d7607f-5fd0-4f4a-b626-d08324aaa805
ms.date: 4/26/2023
ms.keywords: WMCreateDRMTranscryptor, WMCreateDRMTranscryptor function [windows Media Format], wmformat.wmcreatedrmtranscryptor, wmsdkidl/WMCreateDRMTranscryptor
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMCreateDRMTranscryptor
 - wmsdkidl/WMCreateDRMTranscryptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wmvcore.dll
api_name:
 - WMCreateDRMTranscryptor
---

# WMCreateDRMTranscryptor function


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Creates a DRM transcryptor object.

## -parameters

### -param ppTranscryptor [out]

Address of a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmtranscryptor">IWMDRMTranscryptor</a> interface of the newly created DRM transcryptor object.

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The function is unable to allocate memory for the new object.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/wmformat/functions">Functions</a>