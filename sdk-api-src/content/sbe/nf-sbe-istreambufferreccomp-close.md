---
UID: NF:sbe.IStreamBufferRecComp.Close
title: IStreamBufferRecComp::Close
author: windows-sdk-content
description: The Close method closes the target file.
old-location: mstv\istreambufferreccomp_close.htm
tech.root: MSTV
ms.assetid: 0dd311ac-28c7-4cb2-bc65-fe2301c53cf2
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Close, Close method [Microsoft TV Technologies], Close method [Microsoft TV Technologies],IStreamBufferRecComp interface, IStreamBufferRecComp interface [Microsoft TV Technologies],Close method, IStreamBufferRecComp.Close, IStreamBufferRecComp::Close, IStreamBufferRecCompClose, mstv.istreambufferreccomp_close, sbe/IStreamBufferRecComp::Close
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IStreamBufferRecComp.Close
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferRecComp::Close


## -description



The <b>Close</b> method closes the target file.




## -parameters






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



This method is called automatically when the <a href="https://msdn.microsoft.com/4f7fcdee-f6e2-4288-a11c-f0076858be67">RecComp</a> object is released.




## -see-also




<a href="https://msdn.microsoft.com/2998d606-d5ee-4dc3-a4da-57c597c6b594">IStreamBufferRecComp Interface</a>
 

 

