---
UID: NF:wmsdkidl.IWMWriter.AllocateSample
title: IWMWriter::AllocateSample (wmsdkidl.h)
description: The AllocateSample method allocates a buffer that can be used to provide samples to the writer.helpviewer_keywords: ["AllocateSample","AllocateSample method [windows Media Format]","AllocateSample method [windows Media Format]","IWMWriter interface","IWMWriter interface [windows Media Format]","AllocateSample method","IWMWriter.AllocateSample","IWMWriter::AllocateSample","IWMWriterAllocateSample","wmformat.iwmwriter_allocatesample","wmsdkidl/IWMWriter::AllocateSample"]
old-location: wmformat\iwmwriter_allocatesample.htm
tech.root: wmformat
ms.assetid: b23b2364-fb36-479f-bf92-76a5bb4722de
ms.date: 12/05/2018
ms.keywords: AllocateSample, AllocateSample method [windows Media Format], AllocateSample method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],AllocateSample method, IWMWriter.AllocateSample, IWMWriter::AllocateSample, IWMWriterAllocateSample, wmformat.iwmwriter_allocatesample, wmsdkidl/IWMWriter::AllocateSample
f1_keywords:
- wmsdkidl/IWMWriter.AllocateSample
dev_langs:
- c++
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
- IWMWriter.AllocateSample
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriter::AllocateSample


## -description



The <b>AllocateSample</b> method allocates a buffer that can be used to provide samples to the writer.




## -parameters




### -param dwSampleSize [in]

<b>DWORD</b> containing the sample size, in bytes.


### -param ppSample [out]

Pointer to a pointer to an <a href="https://docs.microsoft.com/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer">INSSBuffer</a> interface to an object containing the sample.


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
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The writer is not currently running.

</td>
</tr>
</table>
 




## -remarks



You must use a new buffer for each sample passed to the writer object; reusing a buffer after passing it to call <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-writesample">IWMWriter::WriteSample</a> will cause errors because the writer object does not immediately release its references to the buffer object. You can release the interfaces of the buffer object safely any time after the <b>WriteSample</b> call returns.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter">IWMWriter Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/wmformat/to-write-samples">To Write Samples</a>
 

 

