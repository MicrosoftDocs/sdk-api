---
UID: NF:mfobjects.IMFSample.GetBufferByIndex
title: IMFSample::GetBufferByIndex (mfobjects.h)
description: Gets a buffer from the sample, by index.
helpviewer_keywords: ["48d3b861-96e8-4767-a8b1-65614fd48254","GetBufferByIndex","GetBufferByIndex method [Media Foundation]","GetBufferByIndex method [Media Foundation]","IMFSample interface","IMFSample interface [Media Foundation]","GetBufferByIndex method","IMFSample.GetBufferByIndex","IMFSample::GetBufferByIndex","mf.imfsample_getbufferbyindex","mfobjects/IMFSample::GetBufferByIndex"]
old-location: mf\imfsample_getbufferbyindex.htm
tech.root: medfound
ms.assetid: 48d3b861-96e8-4767-a8b1-65614fd48254
ms.date: 12/05/2018
ms.keywords: 48d3b861-96e8-4767-a8b1-65614fd48254, GetBufferByIndex, GetBufferByIndex method [Media Foundation], GetBufferByIndex method [Media Foundation],IMFSample interface, IMFSample interface [Media Foundation],GetBufferByIndex method, IMFSample.GetBufferByIndex, IMFSample::GetBufferByIndex, mf.imfsample_getbufferbyindex, mfobjects/IMFSample::GetBufferByIndex
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
 - IMFSample::GetBufferByIndex
 - mfobjects/IMFSample::GetBufferByIndex
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
 - IMFSample.GetBufferByIndex
---

# IMFSample::GetBufferByIndex


## -description

Gets a buffer from the sample, by index.


<div class="alert"><b>Note</b>  In most cases, it is safer to use the <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer">IMFSample::ConvertToContiguousBuffer</a> method.  If the sample contains more than one buffer, the <b>ConvertToContiguousBuffer</b> method replaces them with a single buffer, copies the original data into that buffer, and returns the new buffer to the caller. The copy operation occurs at most once. On subsequent calls, no data is copied.</div>
<div> </div>

## -parameters

### -param dwIndex [in]

Index of the buffer. To find the number of buffers in the sample, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getbuffercount">IMFSample::GetBufferCount</a>. Buffers are indexed from zero.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument, or the index is out of range.
              

</td>
</tr>
</table>

## -remarks

A sample might contain more than one buffer. Use the <b>GetBufferByIndex</b> method to enumerate the individual buffers.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfsample">IMFSample</a>



<a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-converttocontiguousbuffer">IMFSample::ConvertToContiguousBuffer</a>



<a href="/windows/desktop/medfound/media-samples">Media Samples</a>