---
UID: NF:mfobjects.IMFSample.CopyToBuffer
title: IMFSample::CopyToBuffer (mfobjects.h)
description: Copies the sample data to a buffer. This method concatenates the valid data from all of the buffers of the sample, in order.
helpviewer_keywords: ["CopyToBuffer","CopyToBuffer method [Media Foundation]","CopyToBuffer method [Media Foundation]","IMFSample interface","IMFSample interface [Media Foundation]","CopyToBuffer method","IMFSample.CopyToBuffer","IMFSample::CopyToBuffer","c8a23e0a-ed2f-449d-b834-f60f383d0b5e","mf.imfsample_copytobuffer","mfobjects/IMFSample::CopyToBuffer"]
old-location: mf\imfsample_copytobuffer.htm
tech.root: mf
ms.assetid: c8a23e0a-ed2f-449d-b834-f60f383d0b5e
ms.date: 12/05/2018
ms.keywords: CopyToBuffer, CopyToBuffer method [Media Foundation], CopyToBuffer method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],CopyToBuffer method, IMFSample.CopyToBuffer, IMFSample::CopyToBuffer, c8a23e0a-ed2f-449d-b834-f60f383d0b5e, mf.imfsample_copytobuffer, mfobjects/IMFSample::CopyToBuffer
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
 - IMFSample::CopyToBuffer
 - mfobjects/IMFSample::CopyToBuffer
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
 - IMFSample.CopyToBuffer
---

# IMFSample::CopyToBuffer


## -description

Copies the sample data to a buffer. This method concatenates the valid data from all of the buffers of the sample, in order.

## -parameters

### -param pBuffer [in]

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface of the destination buffer. The buffer must be large enough to hold the valid data in the sample. To get the size of the data in the sample, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-gettotallength">IMFSample::GetTotalLength</a>.

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to contain the data.

</td>
</tr>
</table>

## -remarks

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>