---
UID: NF:wmcontainer.MFCreateASFMediaSink
title: MFCreateASFMediaSink function (wmcontainer.h)
description: Creates the ASF media sink.
helpviewer_keywords: ["MFCreateASFMediaSink","MFCreateASFMediaSink function [Media Foundation]","d800ac91-f6cc-4f57-9080-4bbafb42d7ed","mf.mfcreateasfmediasink","wmcontainer/MFCreateASFMediaSink"]
old-location: mf\mfcreateasfmediasink.htm
tech.root: mf
ms.assetid: d800ac91-f6cc-4f57-9080-4bbafb42d7ed
ms.date: 12/05/2018
ms.keywords: MFCreateASFMediaSink, MFCreateASFMediaSink function [Media Foundation], d800ac91-f6cc-4f57-9080-4bbafb42d7ed, mf.mfcreateasfmediasink, wmcontainer/MFCreateASFMediaSink
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateASFMediaSink
 - wmcontainer/MFCreateASFMediaSink
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateASFMediaSink
---

# MFCreateASFMediaSink function


## -description

Creates the ASF media sink.

## -parameters

### -param pIByteStream

Pointer to a byte stream that will be used to write the ASF stream.

### -param ppIMediaSink

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a> interface. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
</table>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfbytestream">IMFByteStream</a>



<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasink">IMFMediaSink</a>



<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>