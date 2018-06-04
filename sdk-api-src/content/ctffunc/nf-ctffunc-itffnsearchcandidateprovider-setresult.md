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

# ITfFnSearchCandidateProvider::SetResult


## -description


Provides a text Service or IME with history data when a candidate is chosen by the user.


## -parameters




### -param bstrQuery [in]

The reading string for the text service or IME to convert.


### -param bstrApplicationID [in]

App-specified string that enables a text service or IME to optionally provide different candidates to different apps or contexts based on input history. You can pass an empty <b>BSTR</b>, L””, for a generic context.


### -param bstrResult [in]

A string that represents the candidate string chosen by the user.  It should be one of the candidate string values returned by the <a href="https://msdn.microsoft.com/7D7E8171-229F-4D9C-B086-D68E064A8A4C">GetSearchCandidates</a> method.


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
The method was successful.

</td>
</tr>
</table>
 




## -remarks



Implementing and calling the <a href="https://msdn.microsoft.com/dcc172f9-4fc3-46f4-a1db-0e75fceafb28">SetResult</a> method is optional.

A text service or IME can return <b>E_PENDING</b> if no corresponding call to <a href="https://msdn.microsoft.com/7D7E8171-229F-4D9C-B086-D68E064A8A4C">GetSearchCandidates</a> has been made yet for the value of <i>bstrQuery</i>.




## -see-also




<a href="https://msdn.microsoft.com/7D7E8171-229F-4D9C-B086-D68E064A8A4C">GetSearchCandidates</a>



<a href="https://msdn.microsoft.com/5DD99E0A-42A2-4EA5-B24F-5C439F5D7EEF">ITfFnSearchCandidateProvider</a>
 

 

