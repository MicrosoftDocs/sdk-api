---
UID: NF:sbe.IStreamBufferRecComp.Close
title: IStreamBufferRecComp::Close (sbe.h)
description: The Close method closes the target file.
helpviewer_keywords: ["Close","Close method [Microsoft TV Technologies]","Close method [Microsoft TV Technologies]","IStreamBufferRecComp interface","IStreamBufferRecComp interface [Microsoft TV Technologies]","Close method","IStreamBufferRecComp.Close","IStreamBufferRecComp::Close","IStreamBufferRecCompClose","mstv.istreambufferreccomp_close","sbe/IStreamBufferRecComp::Close"]
old-location: mstv\istreambufferreccomp_close.htm
tech.root: mstv
ms.assetid: 0dd311ac-28c7-4cb2-bc65-fe2301c53cf2
ms.date: 12/05/2018
ms.keywords: Close, Close method [Microsoft TV Technologies], Close method [Microsoft TV Technologies],IStreamBufferRecComp interface, IStreamBufferRecComp interface [Microsoft TV Technologies],Close method, IStreamBufferRecComp.Close, IStreamBufferRecComp::Close, IStreamBufferRecCompClose, mstv.istreambufferreccomp_close, sbe/IStreamBufferRecComp::Close
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStreamBufferRecComp::Close
 - sbe/IStreamBufferRecComp::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Sbe.h
api_name:
 - IStreamBufferRecComp.Close
---

# IStreamBufferRecComp::Close


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>Close</b> method closes the target file.



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

This method is called automatically when the <a href="/previous-versions/windows/desktop/mstv/reccomp-object">RecComp</a> object is released.

## -see-also

<a href="/previous-versions/windows/desktop/api/sbe/nn-sbe-istreambufferreccomp">IStreamBufferRecComp Interface</a>
