---
UID: NF:wmsdkidl.IWMReaderAdvanced.GetStatistics
title: IWMReaderAdvanced::GetStatistics (wmsdkidl.h)
description: The GetStatistics method retrieves the current reader statistics.
helpviewer_keywords: ["GetStatistics","GetStatistics method [windows Media Format]","GetStatistics method [windows Media Format]","IWMReaderAdvanced interface","IWMReaderAdvanced interface [windows Media Format]","GetStatistics method","IWMReaderAdvanced.GetStatistics","IWMReaderAdvanced::GetStatistics","IWMReaderAdvancedGetStatistics","wmformat.iwmreaderadvanced_getstatistics","wmsdkidl/IWMReaderAdvanced::GetStatistics"]
old-location: wmformat\iwmreaderadvanced_getstatistics.htm
tech.root: wmformat
ms.assetid: 9ed2a3fe-c31d-42fc-9ee9-27dd9aef7e06
ms.date: 12/05/2018
ms.keywords: GetStatistics, GetStatistics method [windows Media Format], GetStatistics method [windows Media Format],IWMReaderAdvanced interface, IWMReaderAdvanced interface [windows Media Format],GetStatistics method, IWMReaderAdvanced.GetStatistics, IWMReaderAdvanced::GetStatistics, IWMReaderAdvancedGetStatistics, wmformat.iwmreaderadvanced_getstatistics, wmsdkidl/IWMReaderAdvanced::GetStatistics
f1_keywords:
- wmsdkidl/IWMReaderAdvanced.GetStatistics
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
- IWMReaderAdvanced.GetStatistics
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWMReaderAdvanced::GetStatistics


## -description



The <b>GetStatistics</b> method retrieves the current reader statistics.




## -parameters




### -param pStatistics [in, out]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_reader_statistics">WM_READER_STATISTICS</a> structure.


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
<i>pStatistics</i> is <b>NULL</b>, or the <b>cbSize</b> member of <i>pStatistics</i> is not set to the size of <b>WM_READER_STATISTICS</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method is unable to allocate memory for an internal object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NS_E_INVALID_REQUEST</b></dt>
</dl>
</td>
<td width="60%">
The reader object has not opened a file yet.

</td>
</tr>
</table>
 




## -remarks



The <b>WM_READER_STATISTICS</b> structure must be supplied by the application. The <b>cbSize</b> data member must be set before the structure is passed to the method. The rest of the members will be set by this method.

As with any method, too many calls can affect performance. The actual performance impact is machine-dependent. Using the <b>GetStatistics</b> method for each sample is not recommended. The Microsoft Windows Media Encoder pulls the data once per second, which results in a manageable amount of data being passed.

The <b>GetStatistics</b> method is not recommended for a callback method like <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample">IWMReaderCallback::OnSample</a>. In general, such calls have the potential to lead to deadlocks.

To determine the connection bandwidth before receiving a sample, the <a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreadernetworkconfig-getconnectionbandwidth">IWMReaderNetworkConfig::GetConnectionBandwidth</a> method is the recommended method. The <b>GetStatistics</b> method has more overhead.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced">IWMReaderAdvanced Interface</a>
 

 

