---
UID: NF:strmif.IAMAsyncReaderTimestampScaling.GetTimestampMode
title: IAMAsyncReaderTimestampScaling::GetTimestampMode
author: windows-driver-content
description: Gets the filter's time-stamping mode.
old-location: dshow\iamasyncreadertimestampscaling_gettimestampmode.htm
old-project: DirectShow
ms.assetid: 2fbadd9d-e741-482f-9ff1-655b149fec49
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: FALSE, GetTimestampMode, GetTimestampMode method [DirectShow], GetTimestampMode method [DirectShow],IAMAsyncReaderTimestampScaling interface, IAMAsyncReaderTimestampScaling interface [DirectShow],GetTimestampMode method, IAMAsyncReaderTimestampScaling.GetTimestampMode, IAMAsyncReaderTimestampScaling::GetTimestampMode, TRUE, dshow.iamasyncreadertimestampscaling_gettimestampmode, strmif/IAMAsyncReaderTimestampScaling::GetTimestampMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
-	Strmif.h
api_name:
-	IAMAsyncReaderTimestampScaling.GetTimestampMode
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMAsyncReaderTimestampScaling::GetTimestampMode


## -description


Gets the filter's time-stamping mode.


## -parameters




### -param pfRaw [out]

Receives a Boolean value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b><b>TRUE</b></b></dt>
</dl>
</td>
<td width="60%">
Time stamps are in units of bytes.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b><b>FALSE</b></b></dt>
</dl>
</td>
<td width="60%">
Time stamps are in units of bytes × 10000000. To get the offset in bytes, divide the sample time by 10000000.

</td>
</tr>
</table>
 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/159ed107-383d-4a1a-b172-f2e339d6bc83">IAMAsyncReaderTimestampScaling</a>
 

 

