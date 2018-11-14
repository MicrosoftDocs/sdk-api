---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetFriendlyName
title: IX509EnrollmentPolicyServer::GetFriendlyName
author: windows-sdk-content
description: Retrieves a display name for the certificate enrollment policy (CEP) server.
old-location: security\ix509enrollmentpolicyserver_getfriendlyname.htm
tech.root: SecCertEnroll
ms.assetid: a2e3da49-19b8-44f6-af7c-ec5c13411f3f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetFriendlyName, GetFriendlyName method [Security], GetFriendlyName method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetFriendlyName method, IX509EnrollmentPolicyServer.GetFriendlyName, IX509EnrollmentPolicyServer::GetFriendlyName, certenroll/IX509EnrollmentPolicyServer::GetFriendlyName, security.ix509enrollmentpolicyserver_getfriendlyname
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
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
 - Certenroll.h
api_name:
 - IX509EnrollmentPolicyServer.GetFriendlyName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509EnrollmentPolicyServer.GetFriendlyName
: 
---

# IX509EnrollmentPolicyServer::GetFriendlyName


## -description


The <b>GetFriendlyName</b> method retrieves a display name for the certificate enrollment policy (CEP) server.


## -parameters




### -param pValue [out, retval]

Pointer to a <b>BSTR</b> variable that contains the display name.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The display name could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was not sufficient memory available for the string specified in the <i>pValue</i>  parameter.

</td>
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
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee351692(v=VS.85).aspx">IX509EnrollmentPolicyServer</a>
 

 

