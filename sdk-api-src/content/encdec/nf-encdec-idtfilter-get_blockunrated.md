---
UID: NF:encdec.IDTFilter.get_BlockUnRated
title: IDTFilter::get_BlockUnRated
author: windows-sdk-content
description: The get_BlockUnRated method indicates whether a program without rating information is blocked.
old-location: mstv\idtfilter_get_blockunrated.htm
tech.root: mstv
ms.assetid: 9b8ecc6b-02e8-47e9-a8df-6e73d58dd177
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],get_BlockUnRated method, IDTFilter.get_BlockUnRated, IDTFilter::get_BlockUnRated, IDTFilterget_BlockUnRated, encdec/IDTFilter::get_BlockUnRated, get_BlockUnRated, get_BlockUnRated method [Microsoft TV Technologies], get_BlockUnRated method [Microsoft TV Technologies],IDTFilter interface, mstv.idtfilter_get_blockunrated
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
 - IDTFilter.get_BlockUnRated
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDTFilter::get_BlockUnRated


## -description


The <b>get_BlockUnRated</b> method indicates whether a program without rating information is blocked.


## -parameters




### -param pfBlockUnRatedShows [out, retval]

Receives a Boolean value. If the value is <b>TRUE</b>, unrated shows are blocked. Otherwise, they are not blocked.


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
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The <b>EvalRat</b> object was not successfully created.

</td>
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
</table>
 




## -remarks



The filter passes this call through to the <b>EvalRat</b> object. For more information, see <a href="https://msdn.microsoft.com/f558c87e-59ac-40d3-bfab-2835d59a730b">IEvalRat::get_BlockUnRated</a>.




## -see-also




<a href="https://msdn.microsoft.com/15acf764-7e4d-40c3-b907-ff5dfaa69dae">IDTFilter Interface</a>
 

 

