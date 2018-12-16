---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetMaxStreamSampleSize
title: IWMReaderAdvanced::GetMaxStreamSampleSize
author: windows-sdk-content
description: The GetMaxStreamSampleSize method retrieves the maximum buffer size to be allocated for stream samples for a specified media stream.
old-location: wmformat\iwmreaderadvanced_getmaxstreamsamplesize.htm
tech.root: wmformat
ms.assetid: 9511c269-0f88-4fdd-8d4b-c52bace14791
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetMaxStreamSampleSize, GetMaxStreamSampleSize method [windows Media Format], GetMaxStreamSampleSize method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetMaxStreamSampleSize method, IWMReaderAdvanced.GetMaxStreamSampleSize, IWMReaderAdvanced::GetMaxStreamSampleSize, IWMReaderAdvancedGetMaxStreamSampleSize, wmformat.iwmreaderadvanced_getmaxstreamsamplesize, wmsdkidl/IWMReaderAdvanced::GetMaxStreamSampleSize
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
 - IWMReaderAdvanced.GetMaxStreamSampleSize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMReaderAdvanced::GetMaxStreamSampleSize


## -description



The <b>GetMaxStreamSampleSize</b> method retrieves the maximum buffer size to be allocated for stream samples for a specified media stream.




## -parameters




### -param wStream [in]

Stream number.


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
No file open for stream sample.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>wStream</i> specifies the wrong stream or <i>pcbMax</i> is a <b>NULL</b> pointer.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd757429(v=VS.85).aspx">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743471(v=VS.85).aspx">IWMReaderAdvanced::GetAllocateForStream</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd743473(v=VS.85).aspx">IWMReaderAdvanced::GetMaxOutputSampleSize</a>
 

 

