---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetMaxStreamSampleSize
title: IWMReaderAdvanced::GetMaxStreamSampleSize
author: windows-sdk-content
description: The GetMaxStreamSampleSize method retrieves the maximum buffer size to be allocated for stream samples for a specified media stream.
old-location: wmformat\iwmreaderadvanced_getmaxstreamsamplesize.htm
old-project: wmformat
ms.assetid: 9511c269-0f88-4fdd-8d4b-c52bace14791
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: GetMaxStreamSampleSize, GetMaxStreamSampleSize method [windows Media Format], GetMaxStreamSampleSize method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetMaxStreamSampleSize method, IWMReaderAdvanced.GetMaxStreamSampleSize, IWMReaderAdvanced::GetMaxStreamSampleSize, IWMReaderAdvancedGetMaxStreamSampleSize, wmformat.iwmreaderadvanced_getmaxstreamsamplesize, wmsdkidl/IWMReaderAdvanced::GetMaxStreamSampleSize
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
req.typenames: WM_AETYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wmvcore.lib
-	Wmvcore.dll
-	WMStubDRM.lib
-	WMStubDRM.dll
api_name:
-	IWMReaderAdvanced.GetMaxStreamSampleSize
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
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




<a href="https://msdn.microsoft.com/a7a20f87-6f21-4fe8-8889-1b6689daf833">IWMReaderAdvanced Interface</a>



<a href="https://msdn.microsoft.com/816f13b1-9856-482d-b5b1-4aaf5c61c230">IWMReaderAdvanced::GetAllocateForStream</a>



<a href="https://msdn.microsoft.com/ad21ab6e-c7af-4293-8920-05db62b9f7ef">IWMReaderAdvanced::GetMaxOutputSampleSize</a>
 

 

