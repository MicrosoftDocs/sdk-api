---
UID: NF:tvratings.IEvalRat.put_BlockUnRated
title: IEvalRat::put_BlockUnRated method
author: windows-driver-content
description: The put_BlockUnRated method specifies whether to block a program for which rating information has not been obtained.
old-location: mstv\ievalrat_put_blockunrated.htm
old-project: mstv
ms.assetid: 22f6bc32-3f41-45d4-83e5-f501cbeb772e
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IEvalRat, IEvalRat interface [Microsoft TV Technologies], put_BlockUnRated method, IEvalRat::put_BlockUnRated, IEvalRatput_BlockUnRated, mstv.ievalrat_put_blockunrated, put_BlockUnRated method [Microsoft TV Technologies], put_BlockUnRated method [Microsoft TV Technologies], IEvalRat interface, put_BlockUnRated,IEvalRat.put_BlockUnRated, tvratings/IEvalRat::put_BlockUnRated
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IEvalRat.put_BlockUnRated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEvalRat::put_BlockUnRated method


## -description


The <b>put_BlockUnRated</b> method specifies whether to block a program for which rating information has not been obtained.


## -parameters




### -param fBlockUnRatedShows [in]

Boolean value. Specify <b>TRUE</b> to block unrated programs, or specify <b>FALSE</b> not to block unrated programs.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/b37c7e7d-80fd-4a42-a698-c20ffb2a5052">IEvalRat Interface</a>
 

 

