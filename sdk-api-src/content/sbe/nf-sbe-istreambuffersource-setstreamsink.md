---
UID: NF:sbe.IStreamBufferSource.SetStreamSink
title: IStreamBufferSource::SetStreamSink (sbe.h)
author: windows-sdk-content
description: The SetStreamSink method sets a pointer to the Stream Buffer Sink filter, so that the Stream Buffer Source filter can stream data from the sink filter.
old-location: mstv\istreambuffersource_setstreamsink.htm
tech.root: mstv
ms.assetid: 9cc53fb6-a652-43fa-a962-9bd3c67b5664
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IStreamBufferSource interface [Microsoft TV Technologies],SetStreamSink method, IStreamBufferSource.SetStreamSink, IStreamBufferSource::SetStreamSink, IStreamBufferSourceSetStreamSink, SetStreamSink, SetStreamSink method [Microsoft TV Technologies], SetStreamSink method [Microsoft TV Technologies],IStreamBufferSource interface, mstv.istreambuffersource_setstreamsink, sbe/IStreamBufferSource::SetStreamSink
ms.topic: method
f1_keywords: 
 - "sbe/IStreamBufferSource.SetStreamSink"
dev_langs:
 - c++
req.header: sbe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferSource.SetStreamSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferSource::SetStreamSink


## -description


The <b>SetStreamSink</b> method sets a pointer to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/stream-buffer-sink-filter">Stream Buffer Sink</a> filter, so that the Stream Buffer Source filter can stream data from the sink filter.


## -parameters




### -param pIStreamBufferSink [in]

Pointer to the Stream Buffer Sink filter's <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffersink">IStreamBufferSink Interface</a> interface.


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
</table>
 




## -remarks



The source filter and the sink filter must be within the same process, but can reside in different filter graphs. If they are in different processes, call <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ifilesourcefilter-load">IFileSourceFilter::Load</a> with the same file name used in the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nf-sbe-istreambuffersink-lockprofile">IStreamBufferSink::LockProfile</a> method.

Several Stream Buffer Source filters can stream from the same sink filter.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambuffersource">IStreamBufferSource Interface</a>
 

 

