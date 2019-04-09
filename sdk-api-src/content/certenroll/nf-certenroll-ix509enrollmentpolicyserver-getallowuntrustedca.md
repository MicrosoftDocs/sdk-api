---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetAllowUnTrustedCA
title: IX509EnrollmentPolicyServer::GetAllowUnTrustedCA (certenroll.h)
author: windows-sdk-content
description: Retrieves a value that specifies whether to allow an untrusted certification authority certificate.
old-location: security\ix509enrollmentpolicyserver_getallowuntrustedca.htm
tech.root: seccertenroll
ms.assetid: 6b15a2ba-2e68-4c66-910d-20dd0f0581c2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAllowUnTrustedCA, GetAllowUnTrustedCA method [Security], GetAllowUnTrustedCA method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetAllowUnTrustedCA method, IX509EnrollmentPolicyServer.GetAllowUnTrustedCA, IX509EnrollmentPolicyServer::GetAllowUnTrustedCA, certenroll/IX509EnrollmentPolicyServer::GetAllowUnTrustedCA, security.ix509enrollmentpolicyserver_getallowuntrustedca
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
 - IX509EnrollmentPolicyServer.GetAllowUnTrustedCA
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509EnrollmentPolicyServer::GetAllowUnTrustedCA


## -description


The <b>GetAllowUnTrustedCA</b> method retrieves a value that specifies whether to allow an untrusted certification authority certificate. This value is set by the <a href="https://msdn.microsoft.com/b0d848a2-1bac-4a30-ae02-26d5af719688">Initialize</a> method.


## -parameters




### -param pValue [out, retval]

Pointer to a Boolean value that specifies whether to allow the certificate.


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
 




## -see-also




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

