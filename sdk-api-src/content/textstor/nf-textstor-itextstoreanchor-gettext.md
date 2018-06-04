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

# ITextStoreAnchor::GetText


## -description


The <b>ITextStoreAnchor::GetText</b> method returns information about text at a specified anchor position. This method returns the visible and hidden text and indicates if embedded data is attached to the text.


## -parameters




### -param dwFlags [in]

Not used; should be zero.


### -param paStart [in]

Specifies the starting anchor position.


### -param paEnd [in]

Specifies the ending anchor position. If <b>NULL</b>, it is treated as if it were an anchor positioned at the very end of the text stream.


### -param pchText [out]

Specifies the buffer to receive the text. May be <b>NULL</b> only when <i>cchReq</i> = 0.


### -param cchReq [in]

Specifies the <i>pchText</i> buffer size in characters.


### -param pcch [out]

Receives the number of characters copied into the <i>pchText</i> buffer.


### -param fUpdateAnchor [in]

If <b>TRUE</b>, <i>paStart</i> will be repositioned just past the last character copied to <i>pchText</i>.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The method was unable to obtain a valid interface pointer to <i>paStart</i> and/or <i>paEnd</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_INVALIDPOS</b></dt>
</dl>
</td>
<td width="60%">
The <i>paStart</i> or <i>paEnd</i> anchors are outside of the document text.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TS_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The caller does not have a read-only lock on the document.

</td>
</tr>
</table>
 




## -remarks



Callers that use this method must have a read-only lock on the document by calling the <a href="https://msdn.microsoft.com/4cace5bd-d111-4a9a-af10-9ad454d4f2eb">ITextStoreAnchor::RequestLock</a> method. Without a read-only lock, the method fails and returns <a href="https://msdn.microsoft.com/12178252-c246-4fa4-bf7b-2445b859ec01">TF_E_NOLOCK</a>.

Applications can truncate the method return values for internal reasons.

To quickly scan text with multiple <b>GetText</b> calls, a caller would use <i>fUpdateAnchor</i> = <b>TRUE</b>.

The actual number of characters copied could be less than <i>cchReq</i> if the number of characters between <i>paStart</i> and <i>paEnd</i> is less than <i>cchReq.</i>

The behavior of <b>GetText</b> is not affected by any region boundaries covered by the returned text.




## -see-also




<a href="https://msdn.microsoft.com/62730a6d-4dc8-4207-9818-ab95e6537854">ITextStoreAnchor</a>



<a href="https://msdn.microsoft.com/4cace5bd-d111-4a9a-af10-9ad454d4f2eb">ITextStoreAnchor::RequestLock
      </a>



<a href="https://msdn.microsoft.com/12178252-c246-4fa4-bf7b-2445b859ec01">Manager Return Values</a>



<a href="https://msdn.microsoft.com/601cd6b0-0064-4cd3-99cd-850104a861a5">
        TS_RUNINFO
      </a>
 

 

