---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IInkLineInfo::GetCandidate


## -description



Returns one recognition alternate from the recognition result list.




## -parameters




### -param nCandidateNum [in]

Zero-based index of the alternate list entry to retrieve.


### -param pwcRecogWord [out]

Buffer in which to store the selected recognition alternate. If <i>pwcRecogWord</i> is <b>NULL</b>, the method does not attempt to retrieve the recognition alternate word.


### -param pcwcRecogWord [out]

Passes the length of the <i>pwcRecogWord</i> buffer in Unicode characters, and returns the number of Unicode characters that were copied into the buffer.


### -param dwFlags [in]

Not used.


## -returns



This method can return one of these values.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The <i>nCandidateNum</i> index is greater that the number of recognition alternates.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>pwcRecogWord</i> buffer is not large enough to accept the recognition alternate.

</td>
</tr>
</table>
 




## -remarks



If the <i>pwcRecogWord</i> parameter is null, the method does not attempt to retrieve the recognition alternate word, but only sets <i>pwcRecogWord</i> to the number of characters in the recognition alternate.

If the <i>pwcRecogWord</i> buffer is not large enough to contain the recognition alternate, then the <i>pwcRecogWord</i> buffer is filled with the first <i>pwcRecogWord</i> number of characters from the recognition alternate.




## -see-also




<a href="https://msdn.microsoft.com/58774f49-6af2-4b81-bbd5-709eb694af2d">IInkLineInfo</a>



<a href="https://msdn.microsoft.com/0301706b-6d3e-4fe4-af87-764b1c959707">SetCandidate Method</a>
 

 

