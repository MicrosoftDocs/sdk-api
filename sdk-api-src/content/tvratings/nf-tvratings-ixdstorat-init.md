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

# IXDSToRat::Init


## -description


The <b>Init</b> method sets the <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> object to its initial state.


## -parameters






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
</table>
 




## -remarks



The XDS Codec filter calls this method on startup or after a discontinuity, such as a channel change. The <a href="https://msdn.microsoft.com/bda34c12-0eb8-4d3a-867e-f7215f70c7c7">XDSToRat</a> object should clear any internal buffers and reset its parsing state. This method prevents decoding errors caused by channel changes or other interruptions.




## -see-also




<a href="https://msdn.microsoft.com/de65e5cd-3f4b-4925-a6b8-636fc2e332ec">IXDSToRat Interface</a>
 

 

