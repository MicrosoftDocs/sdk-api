---
UID: NF:wmsdkidl.IWMWriterAdvanced3.GetStatisticsEx
title: IWMWriterAdvanced3::GetStatisticsEx (wmsdkidl.h)
description: The GetStatisticsEx method retrieves extended statistics for the writer.helpviewer_keywords: ["GetStatisticsEx","GetStatisticsEx method [windows Media Format]","GetStatisticsEx method [windows Media Format]","IWMWriterAdvanced3 interface","IWMWriterAdvanced3 interface [windows Media Format]","GetStatisticsEx method","IWMWriterAdvanced3.GetStatisticsEx","IWMWriterAdvanced3::GetStatisticsEx","IWMWriterAdvanced3GetStatisticsEx","wmformat.iwmwriteradvanced3_getstatisticsex","wmsdkidl/IWMWriterAdvanced3::GetStatisticsEx"]
old-location: wmformat\iwmwriteradvanced3_getstatisticsex.htm
tech.root: wmformat
ms.assetid: 3ea41491-409c-42b7-a4b2-f0d7c222c299
ms.date: 12/05/2018
ms.keywords: GetStatisticsEx, GetStatisticsEx method [windows Media Format], GetStatisticsEx method [windows Media Format],IWMWriterAdvanced3 interface, IWMWriterAdvanced3 interface [windows Media Format],GetStatisticsEx method, IWMWriterAdvanced3.GetStatisticsEx, IWMWriterAdvanced3::GetStatisticsEx, IWMWriterAdvanced3GetStatisticsEx, wmformat.iwmwriteradvanced3_getstatisticsex, wmsdkidl/IWMWriterAdvanced3::GetStatisticsEx
f1_keywords:
- wmsdkidl/IWMWriterAdvanced3.GetStatisticsEx
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
- IWMWriterAdvanced3.GetStatisticsEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMWriterAdvanced3::GetStatisticsEx


## -description



The <b>GetStatisticsEx</b> method retrieves extended statistics for the writer.




## -parameters




### -param wStreamNum [in]

<b>WORD</b> containing the stream number for which you want to get statistics. You can pass 0 to obtain extended statistics for the entire file. Stream numbers are in the range of 1 through 63.


### -param pStats [out]

Pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics_ex">WM_WRITER_STATISTICS_EX</a> structure that receives the statistics.


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
The writer is in the configuration state, during which this method cannot be called.

</td>
</tr>
</table>
 




## -remarks



<b>GetStatisticsEx</b> is not an improved version of <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-getstatistics">IWMWriterAdvanced::GetStatistics</a>. The statistics retrieved by <b>GetStatistics</b> are not retrieved by <b>GetStatisticsEx</b>; if you want to get all available statistics you must call both methods.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced3">IWMWriterAdvanced3 Interface</a>
 

 

