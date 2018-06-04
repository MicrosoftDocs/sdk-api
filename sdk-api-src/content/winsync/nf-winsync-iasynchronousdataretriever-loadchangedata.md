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

# IAsynchronousDataRetriever::LoadChangeData


## -description


Retrieves item data for a change.


## -parameters




### -param pLoadChangeContext [in]

Metadata that describes the change for which data should be retrieved.


## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

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
<dt><b>Provider-determined error codes.</b></dt>
</dl>
</td>
<td width="60%">
See Remarks.

</td>
</tr>
</table>
 




## -remarks



When <b>LoadChangeData</b> is called, the provider must take one of the following actions:

<ul>
<li>Return a success code from the method and later call <a href="https://msdn.microsoft.com/b48f9a91-f211-4df4-b315-dfe8d48b3db7">IDataRetrieverCallback::LoadChangeDataComplete</a> to report that asynchronous processing finished successfully.</li>
<li>Return a success code from the method and later call <a href="https://msdn.microsoft.com/93185b3d-458d-4254-af2d-02cf7b1c5be7">IDataRetrieverCallback::LoadChangeDataError</a> to report that an error occurred during asynchronous processing.</li>
<li>Return an error code from the method. In this case, <a href="https://msdn.microsoft.com/fc49614d-fdd7-433a-a942-f442edf1c69f">IDataRetrieverCallback</a> methods should not be called.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/38f07582-908b-430e-a886-c0fc24b807ef">IAsynchronousDataRetriever Interface</a>



<a href="https://msdn.microsoft.com/fc49614d-fdd7-433a-a942-f442edf1c69f">IDataRetrieverCallback Interface</a>
 

 

