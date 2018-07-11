---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetPolicyServerId
title: IX509EnrollmentPolicyServer::GetPolicyServerId
author: windows-sdk-content
description: Retrieves a string value that uniquely identifies the certificate enrollment policy (CEP) server.
old-location: security\ix509enrollmentpolicyserver_getpolicyserverid.htm
old-project: seccertenroll
ms.assetid: daff74e8-a124-4194-95f6-5837598c352f
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: GetPolicyServerId, GetPolicyServerId method [Security], GetPolicyServerId method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetPolicyServerId method, IX509EnrollmentPolicyServer.GetPolicyServerId, IX509EnrollmentPolicyServer::GetPolicyServerId, certenroll/IX509EnrollmentPolicyServer::GetPolicyServerId, security.ix509enrollmentpolicyserver_getpolicyserverid
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509EnrollmentPolicyServer.GetPolicyServerId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509EnrollmentPolicyServer::GetPolicyServerId


## -description


The <b>GetPolicyServerId</b> method retrieves a string value that uniquely identifies the certificate enrollment policy (CEP) server. This value is set in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method.


## -parameters




### -param pValue [out, retval]

Pointer to a <b>BSTR</b> variable that contains the ID string.


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
<dt><b>CERTSRV_E_PROPERTY_EMPTY</b></dt>
</dl>
</td>
<td width="60%">
The ID could not be found.

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




<a href="https://msdn.microsoft.com/e39d40fd-3d43-4cdc-b41a-07a87a11bfad">IX509EnrollmentPolicyServer</a>
 

 

