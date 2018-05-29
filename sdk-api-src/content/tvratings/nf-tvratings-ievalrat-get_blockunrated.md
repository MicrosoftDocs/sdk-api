---
UID: NF:tvratings.IEvalRat.get_BlockUnRated
title: IEvalRat::get_BlockUnRated
author: windows-sdk-content
description: The get_BlockUnRated method indicates whether a program without rating information is blocked.
old-location: mstv\ievalrat_get_blockunrated.htm
old-project: mstv
ms.assetid: f558c87e-59ac-40d3-bfab-2835d59a730b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IEvalRat interface [Microsoft TV Technologies],get_BlockUnRated method, IEvalRat.get_BlockUnRated, IEvalRat::get_BlockUnRated, IEvalRatget_BlockUnRated, get_BlockUnRated, get_BlockUnRated method [Microsoft TV Technologies], get_BlockUnRated method [Microsoft TV Technologies],IEvalRat interface, mstv.ievalrat_get_blockunrated, tvratings/IEvalRat::get_BlockUnRated
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tvratings.h
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
req.typenames: EnTvRat_US_TV
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Tvratings.h
api_name:
-	IEvalRat.get_BlockUnRated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEvalRat::get_BlockUnRated


## -description


The <b>get_BlockUnRated</b> method indicates whether a program without rating information is blocked.


## -parameters




### -param pfBlockUnRatedShows [out, retval]

Receives a Boolean value. If the value is <b>TRUE</b>, unrated shows are blocked. Otherwise, they are not blocked.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
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



<div class="alert"><b>Note</b>  By default, unrated programs should be allowed. Return <b>FALSE</b> in <i>pfBlockUnRatedShows</i> unless the <b>put_BlockUnRated</b> method was previously called with the value <b>TRUE</b>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b37c7e7d-80fd-4a42-a698-c20ffb2a5052">IEvalRat Interface</a>



<a href="https://msdn.microsoft.com/22f6bc32-3f41-45d4-83e5-f501cbeb772e">IEvalRat::put_BlockUnRated</a>
 

 

