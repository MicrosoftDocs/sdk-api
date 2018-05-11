---
UID: NF:strmif.IAMStreamSelect.Count
title: IAMStreamSelect::Count
author: windows-driver-content
description: The Count method retrieves the number of available streams.
old-location: dshow\iamstreamselect_count.htm
old-project: DirectShow
ms.assetid: 5104ce98-5b13-409a-9226-0c089ee8bb1e
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Count, Count method [DirectShow], Count method [DirectShow],IAMStreamSelect interface, IAMStreamSelect interface [DirectShow],Count method, IAMStreamSelect.Count, IAMStreamSelect::Count, IAMStreamSelectCount, dshow.iamstreamselect_count, strmif/IAMStreamSelect::Count
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMStreamSelect.Count
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/a305e91e-f506-4bd1-b4d4-7361df89e158">IAMStreamSelect Interface</a>
 

 

