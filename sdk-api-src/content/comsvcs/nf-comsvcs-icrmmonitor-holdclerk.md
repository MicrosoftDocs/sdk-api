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

# ICrmMonitor::HoldClerk


## -description


Retrieves a pointer on the specified clerk.


## -parameters




### -param Index [in]

A <b>VARIANT</b> string containing the instance CLSID of the required CRM clerk.


### -param pItem [out]

A <b>VARIANT</b> <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer returning the interface to the specified CRM clerk.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_CLERKNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified CRM clerk was not found. It may have completed before it could be held.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ead5f782-8512-4387-b8f3-7be960f35bbe">ICrmMonitor</a>
 

 

