---
UID: NF:strmif.IAMStreamSelect.Count
title: IAMStreamSelect::Count (strmif.h)
author: windows-sdk-content
description: The Count method retrieves the number of available streams.
old-location: dshow\iamstreamselect_count.htm
tech.root: DirectShow
ms.assetid: 5104ce98-5b13-409a-9226-0c089ee8bb1e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Count, Count method [DirectShow], Count method [DirectShow],IAMStreamSelect interface, IAMStreamSelect interface [DirectShow],Count method, IAMStreamSelect.Count, IAMStreamSelect::Count, IAMStreamSelectCount, dshow.iamstreamselect_count, strmif/IAMStreamSelect::Count
ms.topic: method
f1_keywords: 
 - "strmif/IAMStreamSelect.Count"
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMStreamSelect.Count
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMStreamSelect::Count


## -description



The <code>Count</code> method retrieves the number of available streams.




## -parameters




### -param pcStreams [out]

Receives the number of streams.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pins are not connected.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-iamstreamselect">IAMStreamSelect Interface</a>
 

 

