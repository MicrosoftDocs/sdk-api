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

# IX509EnrollmentPolicyServer::GetUseClientId


## -description


The <b>GetUseClientId</b> method retrieves a value that specifies whether the <b>ClientId</b> attribute is set in the policy server flags of the certificate enrollment policy (CEP) server.


## -parameters




### -param pValue [out, retval]

Pointer to a Boolean value that specifies whether the <b>PsfUseClientId</b> bit is set on the <a href="https://msdn.microsoft.com/e73bccb8-ca4d-4007-bdf3-1194ede5fdd1">PolicyServerUrlFlags</a> enumeration for this certificate enrollment policy (CEP) server.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
</table>
 




## -remarks



This method returns <b>VARIANT_TRUE</b> if the <b>PsfUseClientId</b> bit is set on the <a href="https://msdn.microsoft.com/e73bccb8-ca4d-4007-bdf3-1194ede5fdd1">PolicyServerUrlFlags</a> enumeration for this CEP server. If this flag is set, the <b>ClientID</b> attribute is included in certificate requests during the enrollment process and can be used by the certification authority for diagnostic or auditing purposes. Examples of the type of information included in this attribute include the name of the cryptographic service provider, the Windows version number, the user name, the computer DNS name, and the domain controller DNS name.




## -see-also




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

