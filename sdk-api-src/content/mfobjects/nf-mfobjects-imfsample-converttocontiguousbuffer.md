---
UID: NF:mfobjects.IMFSample.ConvertToContiguousBuffer
title: IMFSample::ConvertToContiguousBuffer (mfobjects.h)
description: Converts a sample with multiple buffers into a sample with a single buffer.
helpviewer_keywords: ["6ea950eb-7f2e-4549-93dc-fa62f95b7b66","ConvertToContiguousBuffer","ConvertToContiguousBuffer method [Media Foundation]","ConvertToContiguousBuffer method [Media Foundation]","IMFSample interface","IMFSample interface [Media Foundation]","ConvertToContiguousBuffer method","IMFSample.ConvertToContiguousBuffer","IMFSample::ConvertToContiguousBuffer","mf.imfsample_converttocontiguousbuffer","mfobjects/IMFSample::ConvertToContiguousBuffer"]
old-location: mf\imfsample_converttocontiguousbuffer.htm
tech.root: mf
ms.assetid: 6ea950eb-7f2e-4549-93dc-fa62f95b7b66
ms.date: 12/05/2018
ms.keywords: 6ea950eb-7f2e-4549-93dc-fa62f95b7b66, ConvertToContiguousBuffer, ConvertToContiguousBuffer method [Media Foundation], ConvertToContiguousBuffer method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],ConvertToContiguousBuffer method, IMFSample.ConvertToContiguousBuffer, IMFSample::ConvertToContiguousBuffer, mf.imfsample_converttocontiguousbuffer, mfobjects/IMFSample::ConvertToContiguousBuffer
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
 - IMFSample::ConvertToContiguousBuffer
 - mfobjects/IMFSample::ConvertToContiguousBuffer
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
 - IMFSample.ConvertToContiguousBuffer
---

# IMFSample::ConvertToContiguousBuffer


## -description

Converts a sample with multiple buffers into a sample with a single buffer.

## -parameters

### -param ppBuffer [out]

Receives a pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer">IMFMediaBuffer</a> interface. The caller must release the interface.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The sample does not contain any buffers.

</td>
</tr>
</table>

## -remarks

If the sample contains more than one buffer, this method copies the data from the original buffers into a new buffer, and replaces the original buffer list with the new buffer. The new buffer is returned in the <i>ppBuffer</i> parameter.

If the sample contains a single buffer, this method returns a pointer to the original buffer. In typical use, most samples do not contain multiple buffers.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>