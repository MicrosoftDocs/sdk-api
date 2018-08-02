---
UID: NF:wmsdkidl.IWMWriterPreprocess.PreprocessSample
title: IWMWriterPreprocess::PreprocessSample
author: windows-sdk-content
description: The PreprocessSample method delivers a sample to the writer for preprocessing.
old-location: wmformat\iwmwriterpreprocess_preprocesssample.htm
old-project: wmformat
ms.assetid: 95223ace-0c74-48d8-b49a-98b27c7b735f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWMWriterPreprocess interface [windows Media Format],PreprocessSample method, IWMWriterPreprocess.PreprocessSample, IWMWriterPreprocess::PreprocessSample, IWMWriterPreprocessPreprocessSample, PreprocessSample, PreprocessSample method [windows Media Format], PreprocessSample method [windows Media Format],IWMWriterPreprocess interface, wmformat.iwmwriterpreprocess_preprocesssample, wmsdkidl/IWMWriterPreprocess::PreprocessSample
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 9 Series SDK, or later versions of the SDK
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
 - IWMWriterPreprocess.PreprocessSample
product: Windows
targetos: Windows
req.lib: Wmvcore.lib; WMStubDRM.lib (if you use DRM)
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMWriterPreprocess::PreprocessSample


## -description



The <b>PreprocessSample</b> method delivers a sample to the writer for preprocessing.




## -parameters




### -param dwInputNum [in]

<b>DWORD</b> containing the input number of the sample.


### -param cnsSampleTime [in]

Specifies the presentation time of the sample in 100-nanosecond units.


### -param dwFlags [in]

Reserved. Set to zero.


### -param pSample [in]

Pointer to an <a href="https://msdn.microsoft.com/c47c016a-e7eb-4a2c-b365-5537749db5bc">INSSBuffer</a> interface on an object that contains the sample.


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
<i>dwInputNum</i> specifies an invalid input stream.

OR

<i>pSample</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The writer is not running.

OR

The preprocessor is neither waiting to be run nor stopped in the middle of a pass.

OR

The preprocessor has already made as many passes as specified by <a href="https://msdn.microsoft.com/81ff36e1-cce5-4c99-bf3a-ee2f1050c026">SetNumPreprocessingPasses</a>.

OR

The input specified is not supported for preprocessing.

</td>
</tr>
</table>
 




## -remarks



When performing preprocessing, you should pass the samples for the stream to this method one at a time.




## -see-also




<a href="https://msdn.microsoft.com/06803639-3f21-4003-a460-16a0b5cc6d6f">IWMWriterPreprocess Interface</a>
 

 

