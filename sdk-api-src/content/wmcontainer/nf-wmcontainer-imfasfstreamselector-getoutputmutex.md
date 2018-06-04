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

# IMFASFStreamSelector::GetOutputMutex


## -description



Retrieves a mutual exclusion object for an output.




## -parameters




### -param dwOutputNum [in]

Output number for which to retrieve a mutual exclusion object.


### -param dwMutexNum [in]

Mutual exclusion number. This is an index of mutually exclusive relationships associated with the output. Set to a number between 0, and 1 less than the number of mutual exclusion objects retrieved by calling <a href="https://msdn.microsoft.com/d6e98595-3307-47f5-806d-796350c78cec">IMFASFStreamSelector::GetOutputMutexCount</a>.


### -param ppMutex [out]

Receives a pointer to the mutual exclusion object's <b>IUnknown</b> interface. The caller must release the interface.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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



Outputs are streams in the ASF data section that will be parsed.




## -see-also




<a href="https://msdn.microsoft.com/d2e1fc15-2e12-4698-a4b1-ca8046d228de">IMFASFStreamSelector</a>



<a href="https://msdn.microsoft.com/d6e98595-3307-47f5-806d-796350c78cec">IMFASFStreamSelector::GetOutputMutexCount</a>



<a href="https://msdn.microsoft.com/eebaf4a4-fcd5-4438-82ec-e9da2de6b0fd">IMFASFStreamSelector::SetOutputMutexSelection</a>
 

 

