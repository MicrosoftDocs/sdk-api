---
UID: NF:bdatif.IEnumTuneRequests.Next
title: IEnumTuneRequests::Next
author: windows-sdk-content
description: The Next method retrieves the specified number of items in the collection.
old-location: mstv\ienumtunerequests_next.htm
tech.root: MSTV
ms.assetid: fb846bdb-f0ce-44f7-8d15-608c21e095c1
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IEnumTuneRequests interface [Microsoft TV Technologies],Next method, IEnumTuneRequests.Next, IEnumTuneRequests::Next, IEnumTuneRequestsNext, Next, Next method [Microsoft TV Technologies], Next method [Microsoft TV Technologies],IEnumTuneRequests interface, bdatif/IEnumTuneRequests::Next, mstv.ienumtunerequests_next
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
---

# IEnumTuneRequests::Next


## -description



The <b>Next</b> method retrieves the specified number of items in the collection.




## -parameters




### -param celt [in]

Specifies the number of items to retrieve.


### -param ppprop

TBD


### -param pcelt [out]

Receives the number of items retrieved.


#### - ppProp [out]

Array of size <i>celt</i> that is filled with <a href="https://msdn.microsoft.com/en-us/library/Dd694997(v=VS.85).aspx">ITuneRequest</a> interface pointers.


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




<a href="https://msdn.microsoft.com/en-us/library/Dd375623(v=VS.85).aspx">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd694005(v=VS.85).aspx">IEnumTuneRequests Interface</a>
 

 

