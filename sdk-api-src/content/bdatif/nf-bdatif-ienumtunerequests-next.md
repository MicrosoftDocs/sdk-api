---
UID: NF:bdatif.IEnumTuneRequests.Next
title: IEnumTuneRequests::Next
author: windows-sdk-content
description: The Next method retrieves the specified number of items in the collection.
old-location: mstv\ienumtunerequests_next.htm
old-project: mstv
ms.assetid: fb846bdb-f0ce-44f7-8d15-608c21e095c1
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: IEnumTuneRequests interface [Microsoft TV Technologies],Next method, IEnumTuneRequests.Next, IEnumTuneRequests::Next, IEnumTuneRequestsNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumTuneRequests interface, bdatif/IEnumTuneRequests::Next, mstv.ienumtunerequests_next
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: bdatif.h
req.include-header: 
req.target-type: Windows
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
tech.root: 
req.typenames: SmartCardApplication
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdatif.h
api_name:
 - IEnumTuneRequests.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IEnumTuneRequests::Next


## -description



The <b>Next</b> method retrieves the specified number of items in the collection.




## -parameters




### -param celt [in]

Specifies the number of items to retrieve.


### -param ppprop




### -param pcelt [out]

Receives the number of items retrieved.


#### - ppProp [out]

Array of size <i>celt</i> that is filled with <a href="https://msdn.microsoft.com/34077b45-32b4-466b-b103-6a42fc869265">ITuneRequest</a> interface pointers.


## -returns



The method returns an <b>HRESULT</b>. Possible values include those in the following table.

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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The collection is at the end of the enumeration sequence.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/5ad872be-4408-4069-80db-ae73b2127b91">IEnumTuneRequests Interface</a>
 

 

