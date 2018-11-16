---
UID: NF:sbe.IStreamBufferRecComp.AppendEx
title: IStreamBufferRecComp::AppendEx
author: windows-sdk-content
description: The AppendEx method appends part of a recording to the target file.
old-location: mstv\istreambufferreccomp_appendex.htm
tech.root: mstv
ms.assetid: 9ff4c918-64f7-4c64-b79b-7fe7d7783550
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AppendEx, AppendEx method [Microsoft TV Technologies], AppendEx method [Microsoft TV Technologies],IStreamBufferRecComp interface, IStreamBufferRecComp interface [Microsoft TV Technologies],AppendEx method, IStreamBufferRecComp.AppendEx, IStreamBufferRecComp::AppendEx, IStreamBufferRecCompAppendEx, mstv.istreambufferreccomp_appendex, sbe/IStreamBufferRecComp::AppendEx
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
 - IStreamBufferRecComp.AppendEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- sbe.h
: 
- IStreamBufferRecComp.AppendEx
: 
---

# IStreamBufferRecComp::AppendEx


## -description



The <b>AppendEx</b> method appends part of a recording to the target file.




## -parameters




### -param pszSBRecording [in]

Null-terminated, wide character string that contains the name of the file to append.


### -param rtStart [in]

Specifies the start time of the segment to append, in 100-nanosecond units.


### -param rtStop [in]

Specifies the stop time of the segment to append, in 100-nanosecond units.


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

The value of <i>rtStop</i> must be at least 2 seconds (20000000) greater than <i>rtStart</i>.

The caller must validate <i>rtStart</i> and <i>rtStop</i> before calling this method. The method will not automatically correct the times if they fall past the end of the file.




## -see-also




<a href="https://msdn.microsoft.com/2998d606-d5ee-4dc3-a4da-57c597c6b594">IStreamBufferRecComp Interface</a>
 

 

