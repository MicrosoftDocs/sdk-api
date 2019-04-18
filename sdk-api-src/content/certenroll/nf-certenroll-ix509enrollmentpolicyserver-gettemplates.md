---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetTemplates
title: IX509EnrollmentPolicyServer::GetTemplates (certenroll.h)
author: windows-sdk-content
description: Retrieves a collection of the templates supported by the certificate enrollment policy (CEP) server.
old-location: security\ix509enrollmentpolicyserver_gettemplates.htm
tech.root: seccertenroll
ms.assetid: 52dd85aa-033b-43ab-9b71-1080f969bebc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetTemplates, GetTemplates method [Security], GetTemplates method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetTemplates method, IX509EnrollmentPolicyServer.GetTemplates, IX509EnrollmentPolicyServer::GetTemplates, certenroll/IX509EnrollmentPolicyServer::GetTemplates, security.ix509enrollmentpolicyserver_gettemplates
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
 - IX509EnrollmentPolicyServer.GetTemplates
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509EnrollmentPolicyServer::GetTemplates


## -description


The <b>GetTemplates</b> method retrieves a collection of the templates supported by the certificate enrollment policy (CEP) server.


## -parameters




### -param pTemplates [out, retval]

Address of a variable that receives a pointer to an <a href="https://msdn.microsoft.com/82d14b93-e07b-4ff3-88b9-b1873972b4ad">IX509CertificateTemplates</a> interface that represents the template collection.


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
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a> object has not been initialized.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

