---
UID: NF:wmsdkidl.WMCreateWriterFileSink
title: WMCreateWriterFileSink function (wmsdkidl.h)
description: The WMCreateWriterFileSink function creates a writer file sink object.
helpviewer_keywords: ["WMCreateWriterFileSink","WMCreateWriterFileSink function [windows Media Format]","wmformat.wmcreatewriterfilesink","wmsdkidl/WMCreateWriterFileSink"]
old-location: wmformat\wmcreatewriterfilesink.htm
tech.root: wmformat
ms.assetid: aeeaf67c-119f-482b-b064-87739499abda
ms.date: 12/05/2018
ms.keywords: WMCreateWriterFileSink, WMCreateWriterFileSink function [windows Media Format], wmformat.wmcreatewriterfilesink, wmsdkidl/WMCreateWriterFileSink
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
req.lib: Wmvcore.lib
req.dll: Wmvcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WMCreateWriterFileSink
 - wmsdkidl/WMCreateWriterFileSink
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
 - WMCreateWriterFileSink
---

# WMCreateWriterFileSink function


## -description

The <b>WMCreateWriterFileSink</b> function creates a writer file sink object.

## -parameters

### -param ppSink [out]

Pointer to a pointer to the <a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink">IWMWriterFileSink</a> interface of the newly created writer file sink object.

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



<a href="/windows/desktop/wmformat/writer-file-sink-object">Writer File Sink Object</a>