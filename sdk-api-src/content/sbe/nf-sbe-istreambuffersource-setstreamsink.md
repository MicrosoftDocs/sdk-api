---
UID: NF:sbe.IStreamBufferSource.SetStreamSink
title: IStreamBufferSource::SetStreamSink
author: windows-driver-content
description: The SetStreamSink method sets a pointer to the Stream Buffer Sink filter, so that the Stream Buffer Source filter can stream data from the sink filter.
old-location: mstv\istreambuffersource_setstreamsink.htm
old-project: mstv
ms.assetid: 9cc53fb6-a652-43fa-a962-9bd3c67b5664
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: IStreamBufferSource interface [Microsoft TV Technologies],SetStreamSink method, IStreamBufferSource.SetStreamSink, IStreamBufferSource::SetStreamSink, IStreamBufferSourceSetStreamSink, SetStreamSink, SetStreamSink method [Microsoft TV Technologies], SetStreamSink method [Microsoft TV Technologies],IStreamBufferSource interface, mstv.istreambuffersource_setstreamsink, sbe/IStreamBufferSource::SetStreamSink
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: STREAMBUFFER_ATTR_DATATYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sbe.h
api_name:
-	IStreamBufferSource.SetStreamSink
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IStreamBufferSource::SetStreamSink


## -description


The <b>SetStreamSink</b> method sets a pointer to the <a href="https://msdn.microsoft.com/e49fe3c2-e77f-419a-910c-78f72ebdfdbc">Stream Buffer Sink</a> filter, so that the Stream Buffer Source filter can stream data from the sink filter.


## -parameters




### -param pIStreamBufferSink [in]

Pointer to the Stream Buffer Sink filter's <a href="https://msdn.microsoft.com/4ae5a9e9-da51-4034-9a2c-22b57374deac">IStreamBufferSink Interface</a> interface.


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



The source filter and the sink filter must be within the same process, but can reside in different filter graphs. If they are in different processes, call <a href="https://msdn.microsoft.com/a44b8153-19d5-43ad-936c-214c694eeeb6">IFileSourceFilter::Load</a> with the same file name used in the <a href="https://msdn.microsoft.com/9e694cc2-090e-43b1-88c7-77175a930bf1">IStreamBufferSink::LockProfile</a> method.

Several Stream Buffer Source filters can stream from the same sink filter.




## -see-also




<a href="https://msdn.microsoft.com/1e407f85-820a-4d17-926d-0c00e1e453e2">IStreamBufferSource Interface</a>
 

 

