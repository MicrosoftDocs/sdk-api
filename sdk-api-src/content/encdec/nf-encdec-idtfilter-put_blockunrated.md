---
UID: NF:encdec.IDTFilter.put_BlockUnRated
title: IDTFilter::put_BlockUnRated
author: windows-sdk-content
description: The put_BlockUnRated method specifies whether to block a program for which rating information has not been obtained.
old-location: mstv\idtfilter_put_blockunrated.htm
old-project: mstv
ms.assetid: 2b6ef516-bbc8-4d17-a306-433e8265e879
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IDTFilter interface [Microsoft TV Technologies],put_BlockUnRated method, IDTFilter.put_BlockUnRated, IDTFilter::put_BlockUnRated, IDTFilterput_BlockUnRated, encdec/IDTFilter::put_BlockUnRated, mstv.idtfilter_put_blockunrated, put_BlockUnRated, put_BlockUnRated method [Microsoft TV Technologies], put_BlockUnRated method [Microsoft TV Technologies],IDTFilter interface
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ProtType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IDTFilter.put_BlockUnRated
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDTFilter::put_BlockUnRated


## -description


The <b>put_BlockUnRated</b> method specifies whether to block a program for which rating information has not been obtained.


## -parameters




### -param fBlockUnRatedShows [in]

Boolean value. Specify <b>TRUE</b> to block unrated programs, or specify <b>FALSE</b> not to block unrated programs.


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



The filter passes this call through to the <b>EvalRat</b> object. For more information, see <a href="https://msdn.microsoft.com/22f6bc32-3f41-45d4-83e5-f501cbeb772e">IEvalRat::put_BlockUnRated</a>.




## -see-also




<a href="https://msdn.microsoft.com/15acf764-7e4d-40c3-b907-ff5dfaa69dae">IDTFilter Interface</a>
 

 

