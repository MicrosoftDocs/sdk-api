---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetMaxOutputSampleSize
title: IWMReaderAdvanced::GetMaxOutputSampleSize
author: windows-sdk-content
description: The GetMaxOutputSampleSize method retrieves the maximum buffer size to be allocated for output samples for a specified media stream.
old-location: wmformat\iwmreaderadvanced_getmaxoutputsamplesize.htm
tech.root: wmformat
ms.assetid: ad21ab6e-c7af-4293-8920-05db62b9f7ef
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMaxOutputSampleSize, GetMaxOutputSampleSize method [windows Media Format], GetMaxOutputSampleSize method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetMaxOutputSampleSize method, IWMReaderAdvanced.GetMaxOutputSampleSize, IWMReaderAdvanced::GetMaxOutputSampleSize, IWMReaderAdvancedGetMaxOutputSampleSize, wmformat.iwmreaderadvanced_getmaxoutputsamplesize, wmsdkidl/IWMReaderAdvanced::GetMaxOutputSampleSize
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWMReaderAdvanced.GetMaxOutputSampleSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced::GetMaxOutputSampleSize


## -description



The <b>GetMaxOutputSampleSize</b> method retrieves the maximum buffer size to be allocated for output samples for a specified media stream.




## -parameters




### -param dwOutput [in]

<b>DWORD</b> specifying the output media stream.


### -param pcbMax [out]

Pointer to the maximum buffer size to be allocated.


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
<dt><b>ASF_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
No file has been opened for the sample.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>dwOutput</i> specifies the wrong output or <i>pcbMax</i> is a <b>NULL</b> pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/b0da74ff-37d9-4bb3-85f2-f8e1585c2d7f">IWMReaderAdvanced::GetAllocateForOutput</a>



<a href="https://msdn.microsoft.com/9511c269-0f88-4fdd-8d4b-c52bace14791">IWMReaderAdvanced::GetMaxStreamSampleSize</a>
 

 

