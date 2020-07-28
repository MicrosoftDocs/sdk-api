---
UID: NF:sbe.IStreamBufferRecComp.GetCurrentLength
title: IStreamBufferRecComp::GetCurrentLength (sbe.h)
description: The GetCurrentLength method retrieves the length of the target file.
helpviewer_keywords: ["GetCurrentLength","GetCurrentLength method [Microsoft TV Technologies]","GetCurrentLength method [Microsoft TV Technologies]","IStreamBufferRecComp interface","IStreamBufferRecComp interface [Microsoft TV Technologies]","GetCurrentLength method","IStreamBufferRecComp.GetCurrentLength","IStreamBufferRecComp::GetCurrentLength","IStreamBufferRecCompGetCurrentLength","mstv.istreambufferreccomp_getcurrentlength","sbe/IStreamBufferRecComp::GetCurrentLength"]
old-location: mstv\istreambufferreccomp_getcurrentlength.htm
tech.root: mstv
ms.assetid: d482bddc-3754-4d3c-8a9b-c0dc0afb00bb
ms.date: 12/05/2018
ms.keywords: GetCurrentLength, GetCurrentLength method [Microsoft TV Technologies], GetCurrentLength method [Microsoft TV Technologies],IStreamBufferRecComp interface, IStreamBufferRecComp interface [Microsoft TV Technologies],GetCurrentLength method, IStreamBufferRecComp.GetCurrentLength, IStreamBufferRecComp::GetCurrentLength, IStreamBufferRecCompGetCurrentLength, mstv.istreambufferreccomp_getcurrentlength, sbe/IStreamBufferRecComp::GetCurrentLength
f1_keywords:
- sbe/IStreamBufferRecComp.GetCurrentLength
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
- IStreamBufferRecComp.GetCurrentLength
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBufferRecComp::GetCurrentLength


## -description



The <b>GetCurrentLength</b> method retrieves the length of the target file.




## -parameters




### -param pcSeconds [out]

Pointer to a variable that receives the current length, in seconds.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those in the following table.

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
Success

</td>
</tr>
</table>
 




## -remarks



To get accurate updates, you can call this method continually from one thread while another thread performs append operations.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferreccomp">IStreamBufferRecComp Interface</a>
 

 

