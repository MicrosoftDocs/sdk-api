---
UID: NF:encdec.IDTFilter.put_BlockUnRatedDelay
title: IDTFilter::put_BlockUnRatedDelay
author: windows-sdk-content
description: The put_BlockUnRatedDelay method sets the length of time the filter waits before it blocks unrated content.
old-location: mstv\idtfilter_put_blockunrateddelay.htm
tech.root: MSTV
ms.assetid: 2caabce8-57b0-4a43-87b7-1b045ca573db
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],put_BlockUnRatedDelay method, IDTFilter.put_BlockUnRatedDelay, IDTFilter::put_BlockUnRatedDelay, IDTFilterput_BlockUnRatedDelay, encdec/IDTFilter::put_BlockUnRatedDelay, mstv.idtfilter_put_blockunrateddelay, put_BlockUnRatedDelay, put_BlockUnRatedDelay method [Microsoft TV Technologies], put_BlockUnRatedDelay method [Microsoft TV Technologies],IDTFilter interface
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: encdec.h
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
 - EncDec.h
api_name:
 - IDTFilter.put_BlockUnRatedDelay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- encdec.h
: 
- IDTFilter.put_BlockUnRatedDelay
: 
---

# IDTFilter::put_BlockUnRatedDelay


## -description


The <b>put_BlockUnRatedDelay</b> method sets the length of time the filter waits before it blocks unrated content.


## -parameters




### -param msecsDelayBeforeBlock [in]

Specifies the delay, in milliseconds. The value must be from 0 to 60000 (60 seconds).


## -returns



Returns an <b>HRESULT</b>. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks



Regardless of the value of this property, the filter does not block unrated content unless the <b>BlockUnRated</b> property is <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/15acf764-7e4d-40c3-b907-ff5dfaa69dae">IDTFilter Interface</a>



<a href="https://msdn.microsoft.com/2b6ef516-bbc8-4d17-a306-433e8265e879">IDTFilter::put_BlockUnRated</a>
 

 

