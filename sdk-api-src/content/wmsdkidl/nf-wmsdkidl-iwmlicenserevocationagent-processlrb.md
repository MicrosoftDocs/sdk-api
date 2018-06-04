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

# IWMLicenseRevocationAgent::ProcessLRB


## -description



The <b>ProcessLRB</b> method removes licenses from the license store on the client computer.




## -parameters




### -param pSignedLRB [in]

Address of the signed license revocation blob in memory. This blob is sent to your application by the license server.


### -param dwSignedLRBLength [in]

Size of the license revocation blob in bytes.


### -param pSignedACK [out]

Address of a buffer that receives the signed acknowledgement of license revocation. Your application must send the acknowledgement to the license server.


### -param pdwSignedACKLength [out]

Size of the acknowledgement in bytes.


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



The license server sends the signed license revocation blob after receiving a response to its initial challenge message. For more information, see <a href="https://msdn.microsoft.com/9006f6c5-f9e7-4d00-a7c2-bbdfcfdd85e7">GetLRBChallenge</a>.




## -see-also




<a href="https://msdn.microsoft.com/4cb5beb9-72b8-46cb-8460-56455785a7a0">IWMLicenseRevocationAgent Interface</a>
 

 

