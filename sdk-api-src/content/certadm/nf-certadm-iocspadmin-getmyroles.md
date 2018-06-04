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

# IOCSPAdmin::GetMyRoles


## -description


The <b>GetMyRoles</b> method gets the access mask of privilege roles for a user on a given Online Certificate Status Protocol (OCSP) responder server.


## -parameters




### -param bstrServerName [in]

A string that contains the responder-server name.


### -param pRoles [out]

A pointer to the 32-bit access mask.


## -returns



<h3>C++</h3>
 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
The 32-bit access mask.



## -remarks



The OCSP responder server defines the following masks for access privilege roles.

<table>
<tr>
<th>Constant</th>
<th>C++ value</th>
<th>VB Script value</th>
<th>Description</th>
</tr>
<tr>
<td>
CA_ACCESS_ADMIN

</td>
<td>
0x001

</td>
<td>
&amp;H1

</td>
<td>
CA administrator

</td>
</tr>
<tr>
<td>
CA_ACCESS_READ

</td>
<td>
0x100

</td>
<td>
&amp;H100

</td>
<td>
Read-only access to a CA

</td>
</tr>
<tr>
<td>
CA_ACCESS_ENROLL

</td>
<td>
0x200

</td>
<td>
&amp;H200

</td>
<td>
Enroll access to a CA

</td>
</tr>
</table>
 

Examples of privileges a user might have, depending on the  mask:

<ul>
<li>Configure and upgrade an OCSP server.</li>
<li>Assign existing signing certificate and key.</li>
<li>Install and update Certificate Revocation Lists (CRLs).</li>
<li>Configure a  response format.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/cf76e934-07a2-46de-b2cf-7f6d3e274d71">IOCSPAdmin</a>
 

 

