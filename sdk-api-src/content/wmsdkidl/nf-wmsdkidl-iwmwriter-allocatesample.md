---
UID: NF:wmsdkidl.IWMWriter.AllocateSample
title: IWMWriter::AllocateSample
author: windows-sdk-content
description: The AllocateSample method allocates a buffer that can be used to provide samples to the writer.
old-location: wmformat\iwmwriter_allocatesample.htm
old-project: wmformat
ms.assetid: b23b2364-fb36-479f-bf92-76a5bb4722de
ms.author: windowssdkdev
ms.date: 07/02/2018
ms.keywords: AllocateSample, AllocateSample method [windows Media Format], AllocateSample method [windows Media Format],IWMWriter interface, IWMWriter interface [windows Media Format],AllocateSample method, IWMWriter.AllocateSample, IWMWriter::AllocateSample, IWMWriterAllocateSample, wmformat.iwmwriter_allocatesample, wmsdkidl/IWMWriter::AllocateSample
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WM_AETYPE
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
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriter::AllocateSample


## -description



The <b>AllocateSample</b> method allocates a buffer that can be used to provide samples to the writer.




## -parameters




### -param dwSampleSize [in]

<b>DWORD</b> containing the sample size, in bytes.


### -param ppSample [out]

Pointer to a pointer to an <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface to an object containing the sample.


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



You must use a new buffer for each sample passed to the writer object; reusing a buffer after passing it to call <a href="https://msdn.microsoft.com/ba1cf121-1d01-4e90-9ab0-95af0b6e3850">IWMWriter::WriteSample</a> will cause errors because the writer object does not immediately release its references to the buffer object. You can release the interfaces of the buffer object safely any time after the <b>WriteSample</b> call returns.




## -see-also




<a href="https://msdn.microsoft.com/a194ef11-5203-4e85-af91-cdce0c53fe76">IWMWriter Interface</a>



<a href="https://msdn.microsoft.com/9ce10a77-9e80-45e0-a7e7-2ffdf8b57773">To Write Samples</a>
 

 

