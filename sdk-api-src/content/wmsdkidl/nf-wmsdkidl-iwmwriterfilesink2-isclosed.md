---
UID: NF:wmsdkidl.IWMWriterFileSink2.IsClosed
title: IWMWriterFileSink2::IsClosed (wmsdkidl.h)
description: The IsClosed method ascertains whether the file sink has been closed.
helpviewer_keywords: ["IWMWriterFileSink2 interface [windows Media Format]","IsClosed method","IWMWriterFileSink2.IsClosed","IWMWriterFileSink2::IsClosed","IWMWriterFileSink2IsClosed","IsClosed","IsClosed method [windows Media Format]","IsClosed method [windows Media Format]","IWMWriterFileSink2 interface","wmformat.iwmwriterfilesink2_isclosed","wmsdkidl/IWMWriterFileSink2::IsClosed"]
old-location: wmformat\iwmwriterfilesink2_isclosed.htm
tech.root: wmformat
ms.assetid: 0ae9137f-ce43-4860-a28f-deac39f216a4
ms.date: 12/05/2018
ms.keywords: IWMWriterFileSink2 interface [windows Media Format],IsClosed method, IWMWriterFileSink2.IsClosed, IWMWriterFileSink2::IsClosed, IWMWriterFileSink2IsClosed, IsClosed, IsClosed method [windows Media Format], IsClosed method [windows Media Format],IWMWriterFileSink2 interface, wmformat.iwmwriterfilesink2_isclosed, wmsdkidl/IWMWriterFileSink2::IsClosed
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
 - IWMWriterFileSink2::IsClosed
 - wmsdkidl/IWMWriterFileSink2::IsClosed
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
 - IWMWriterFileSink2.IsClosed
---

# IWMWriterFileSink2::IsClosed


## -description

The <b>IsClosed</b> method ascertains whether the file sink has been closed.

## -parameters

### -param pfClosed [out]

Pointer to a Boolean value that is set to True if the file sink has been closed.

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
The <i>pfClosed</i> parameter is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2">IWMWriterFileSink2 Interface</a>