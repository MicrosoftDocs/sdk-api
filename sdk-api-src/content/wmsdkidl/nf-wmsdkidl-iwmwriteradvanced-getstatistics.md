---
UID: NF:wmsdkidl.IWMWriterAdvanced.GetStatistics
title: IWMWriterAdvanced::GetStatistics (wmsdkidl.h)
description: The GetStatistics method retrieves statistics describing the current writing operation.
helpviewer_keywords: ["GetStatistics","GetStatistics method [windows Media Format]","GetStatistics method [windows Media Format]","IWMWriterAdvanced interface","IWMWriterAdvanced interface [windows Media Format]","GetStatistics method","IWMWriterAdvanced.GetStatistics","IWMWriterAdvanced::GetStatistics","IWMWriterAdvancedGetStatistics","wmformat.iwmwriteradvanced_getstatistics","wmsdkidl/IWMWriterAdvanced::GetStatistics"]
old-location: wmformat\iwmwriteradvanced_getstatistics.htm
tech.root: wmformat
ms.assetid: 005c2039-e821-42ab-bead-1bf40f2ab171
ms.date: 12/05/2018
ms.keywords: GetStatistics, GetStatistics method [windows Media Format], GetStatistics method [windows Media Format],IWMWriterAdvanced interface, IWMWriterAdvanced interface [windows Media Format],GetStatistics method, IWMWriterAdvanced.GetStatistics, IWMWriterAdvanced::GetStatistics, IWMWriterAdvancedGetStatistics, wmformat.iwmwriteradvanced_getstatistics, wmsdkidl/IWMWriterAdvanced::GetStatistics
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWMWriterAdvanced::GetStatistics
 - wmsdkidl/IWMWriterAdvanced::GetStatistics
dev_langs:
 - c++
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
 - IWMWriterAdvanced.GetStatistics
---

# IWMWriterAdvanced::GetStatistics


## -description

The <b>GetStatistics</b> method retrieves statistics describing the current writing operation.

## -parameters

### -param wStreamNum [in]

<b>WORD</b> containing the stream number. Stream numbers must be in the range of 1 through 63. A value of 0 retrieves statistics for the file as a whole.

### -param pStats [out]

Pointer to a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_writer_statistics">WM_WRITER_STATISTICS</a> structure that receives the statistics.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<i>pStats</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced">IWMWriterAdvanced Interface</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriteradvanced3-getstatisticsex">IWMWriterAdvanced3::GetStatisticsEx</a>