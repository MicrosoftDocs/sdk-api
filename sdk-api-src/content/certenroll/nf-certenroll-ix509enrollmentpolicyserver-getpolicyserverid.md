---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetPolicyServerId
title: IX509EnrollmentPolicyServer::GetPolicyServerId (certenroll.h)
description: Retrieves a string value that uniquely identifies the certificate enrollment policy (CEP) server.
helpviewer_keywords: ["GetPolicyServerId","GetPolicyServerId method [Security]","GetPolicyServerId method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetPolicyServerId method","IX509EnrollmentPolicyServer.GetPolicyServerId","IX509EnrollmentPolicyServer::GetPolicyServerId","certenroll/IX509EnrollmentPolicyServer::GetPolicyServerId","security.ix509enrollmentpolicyserver_getpolicyserverid"]
old-location: security\ix509enrollmentpolicyserver_getpolicyserverid.htm
tech.root: security
ms.assetid: daff74e8-a124-4194-95f6-5837598c352f
ms.date: 12/05/2018
ms.keywords: GetPolicyServerId, GetPolicyServerId method [Security], GetPolicyServerId method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetPolicyServerId method, IX509EnrollmentPolicyServer.GetPolicyServerId, IX509EnrollmentPolicyServer::GetPolicyServerId, certenroll/IX509EnrollmentPolicyServer::GetPolicyServerId, security.ix509enrollmentpolicyserver_getpolicyserverid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509EnrollmentPolicyServer::GetPolicyServerId
 - certenroll/IX509EnrollmentPolicyServer::GetPolicyServerId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certenroll.h
api_name:
 - IX509EnrollmentPolicyServer.GetPolicyServerId
---

# IX509EnrollmentPolicyServer::GetPolicyServerId


## -description

The <b>GetPolicyServerId</b> method retrieves a string value that uniquely identifies the certificate enrollment policy (CEP) server. This value is set in the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-initialize">Initialize</a> method.

## -parameters

### -param pValue [out, retval]

Pointer to a <b>BSTR</b> variable that contains the ID string.

## -returns

If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table.  For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

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

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>