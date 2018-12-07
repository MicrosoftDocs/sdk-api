---
UID: NF:sbe.IStreamBufferRecComp.Append
title: IStreamBufferRecComp::Append
author: windows-sdk-content
description: The Append method appends an entire recording to the target file.
old-location: mstv\istreambufferreccomp_append.htm
tech.root: mstv
ms.assetid: 17911b5d-6ef5-45d2-83c3-e1b481544008
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Append, Append method [Microsoft TV Technologies], Append method [Microsoft TV Technologies],IStreamBufferRecComp interface, IStreamBufferRecComp interface [Microsoft TV Technologies],Append method, IStreamBufferRecComp.Append, IStreamBufferRecComp::Append, IStreamBufferRecCompAppend, mstv.istreambufferreccomp_append, sbe/IStreamBufferRecComp::Append
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
 - IStreamBufferRecComp.Append
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStreamBufferRecComp::Append


## -description



The <b>Append</b> method appends an entire recording to the target file.




## -parameters




### -param pszSBRecording [in]

Null-terminated, wide character string that contains the name of the file to append.


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



The file specified in <i>pszSBRecording</i> must be completed. If the file is live, the method fails. Also, the file's profile must match the one that was configured in the <b>Initialize</b> method.




## -see-also




<a href="https://msdn.microsoft.com/2998d606-d5ee-4dc3-a4da-57c597c6b594">IStreamBufferRecComp Interface</a>
 

 

