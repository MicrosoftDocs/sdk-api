---
UID: NF:mfobjects.IMFSample.AddBuffer
title: IMFSample::AddBuffer (mfobjects.h)
description: Adds a buffer to the end of the list of buffers in the sample.
helpviewer_keywords: ["61c2a1dc-b9fe-4296-bf33-d54006cad32b","AddBuffer","AddBuffer method [Media Foundation]","AddBuffer method [Media Foundation]","IMFSample interface","IMFSample interface [Media Foundation]","AddBuffer method","IMFSample.AddBuffer","IMFSample::AddBuffer","mf.imfsample_addbuffer","mfobjects/IMFSample::AddBuffer"]
old-location: mf\imfsample_addbuffer.htm
tech.root: mf
ms.assetid: 61c2a1dc-b9fe-4296-bf33-d54006cad32b
ms.date: 12/05/2018
ms.keywords: 61c2a1dc-b9fe-4296-bf33-d54006cad32b, AddBuffer, AddBuffer method [Media Foundation], AddBuffer method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],AddBuffer method, IMFSample.AddBuffer, IMFSample::AddBuffer, mf.imfsample_addbuffer, mfobjects/IMFSample::AddBuffer
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFSample::AddBuffer
 - mfobjects/IMFSample::AddBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFSample.AddBuffer
---

# IMFSample::AddBuffer


## -description

Adds a buffer to the end of the list of buffers in the sample.

## -parameters

### -param pBuffer [in]

Pointer to the buffer's <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface.

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
NULL pointer argument.

</td>
</tr>
</table>

## -remarks

For uncompressed video data, each buffer should contain a single video frame, and samples should not contain multiple frames. In general, storing multiple buffers in a sample is discouraged.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>