---
UID: NF:wmsdkidl.IWMSyncReader.GetMaxStreamSampleSize
title: IWMSyncReader::GetMaxStreamSampleSize (wmsdkidl.h)
description: The GetMaxStreamSampleSize method retrieves the maximum sample size for a specified stream in the file that is open in the synchronous reader.helpviewer_keywords: ["GetMaxStreamSampleSize","GetMaxStreamSampleSize method [windows Media Format]","GetMaxStreamSampleSize method [windows Media Format]","IWMSyncReader interface","IWMSyncReader interface [windows Media Format]","GetMaxStreamSampleSize method","IWMSyncReader.GetMaxStreamSampleSize","IWMSyncReader::GetMaxStreamSampleSize","IWMSyncReaderGetMaxStreamSampleSize","wmformat.iwmsyncreader_getmaxstreamsamplesize","wmsdkidl/IWMSyncReader::GetMaxStreamSampleSize"]
old-location: wmformat\iwmsyncreader_getmaxstreamsamplesize.htm
tech.root: wmformat
ms.assetid: 8b098985-4eb2-4292-a9b9-cfdd051e9c0e
ms.date: 12/05/2018
ms.keywords: GetMaxStreamSampleSize, GetMaxStreamSampleSize method [windows Media Format], GetMaxStreamSampleSize method [windows Media Format],IWMSyncReader interface, IWMSyncReader interface [windows Media Format],GetMaxStreamSampleSize method, IWMSyncReader.GetMaxStreamSampleSize, IWMSyncReader::GetMaxStreamSampleSize, IWMSyncReaderGetMaxStreamSampleSize, wmformat.iwmsyncreader_getmaxstreamsamplesize, wmsdkidl/IWMSyncReader::GetMaxStreamSampleSize
f1_keywords:
- wmsdkidl/IWMSyncReader.GetMaxStreamSampleSize
dev_langs:
- c++
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
- IWMSyncReader.GetMaxStreamSampleSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMSyncReader::GetMaxStreamSampleSize


## -description



The <b>GetMaxStreamSampleSize</b> method retrieves the maximum sample size for a specified stream in the file that is open in the synchronous reader.




## -parameters




### -param wStream [in]

<b>WORD</b> containing the stream number for which you want to retrieve the maximum sample size.


### -param pcbMax [out]

Pointer to a <b>DWORD</b> value that receives the maximum sample size, in bytes, for the stream specified in <i>wStream</i>.


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
<i>pcbMax</i> is <b>NULL</b>.

OR

<i>wStream</i> specifies an invalid stream number.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ASF_E_INVALIDSTATE</b></dt>
</dl>
</td>
<td width="60%">
No file is open in the synchronous reader.

</td>
</tr>
</table>
 




## -remarks



This method retrieves the maximum sample size for an individual stream. The stream may be one of several in an output. If you are using output numbers, you should use <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize">IWMSyncReader::GetMaxOutputSampleSize</a> to retrieve the maximum sample size for the entire output.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader">IWMSyncReader Interface</a>
 

 

