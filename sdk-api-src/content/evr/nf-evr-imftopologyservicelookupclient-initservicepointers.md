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

# IMFTopologyServiceLookupClient::InitServicePointers


## -description



Signals the mixer or presenter to query the enhanced video renderer (EVR) for interface pointers.




## -parameters




### -param pLookup [in]

Pointer to the <a href="https://msdn.microsoft.com/a912c17a-40ef-441c-bfc9-7ef49d22070f">IMFTopologyServiceLookup</a> interface. To query the EVR for an interface, call <a href="https://msdn.microsoft.com/ba0dbfdf-1bab-42ba-910f-04a3f37be955">IMFTopologyServiceLookup::LookupService</a>.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

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
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/a912c17a-40ef-441c-bfc9-7ef49d22070f">IMFTopologyServiceLookup</a> pointer is guaranteed to be valid only during the call to <b>InitServicePointers</b>. The mixer or presenter should not store a pointer to this interface after the method returns.

When the EVR calls <a href="https://msdn.microsoft.com/03ed29b4-89c1-4702-a23f-d013eeef5d44">IMFTopologyServiceLookupClient::ReleaseServicePointers</a>, the mixer or presenter should release any pointers it obtained from the EVR.




## -see-also




<a href="https://msdn.microsoft.com/1135b309-b158-4b70-9f76-5c93d0ad3250">How to Write an EVR Presenter</a>



<a href="https://msdn.microsoft.com/c4215d08-3734-44b9-b053-0d49d89a90f6">IMFTopologyServiceLookupClient</a>
 

 

