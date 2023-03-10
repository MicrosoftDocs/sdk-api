---
UID: NF:certenroll.IX509EnrollmentPolicyServer.Validate
title: IX509EnrollmentPolicyServer::Validate (certenroll.h)
description: Validates the current policy information.
helpviewer_keywords: ["IX509EnrollmentPolicyServer interface [Security]","Validate method","IX509EnrollmentPolicyServer.Validate","IX509EnrollmentPolicyServer::Validate","Validate","Validate method [Security]","Validate method [Security]","IX509EnrollmentPolicyServer interface","certenroll/IX509EnrollmentPolicyServer::Validate","security.ix509enrollmentpolicyserver_validate"]
old-location: security\ix509enrollmentpolicyserver_validate.htm
tech.root: security
ms.assetid: ab58622e-79a6-4a1b-a0e2-74efb81c7062
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentPolicyServer interface [Security],Validate method, IX509EnrollmentPolicyServer.Validate, IX509EnrollmentPolicyServer::Validate, Validate, Validate method [Security], Validate method [Security],IX509EnrollmentPolicyServer interface, certenroll/IX509EnrollmentPolicyServer::Validate, security.ix509enrollmentpolicyserver_validate
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
 - IX509EnrollmentPolicyServer::Validate
 - certenroll/IX509EnrollmentPolicyServer::Validate
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
 - IX509EnrollmentPolicyServer.Validate
---

# IX509EnrollmentPolicyServer::Validate


## -description

The <b>Validate</b> method validates the current policy information.



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
<dt><b>E_NOT_VALID_STATE</b></dt>
</dl>
</td>
<td width="60%">
There was a problem with the lightweight directory access protocol (LDAP) used to locate the CEP server.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> has been initialized by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-initializeimport">InitializeImport</a> method.

</td>
</tr>
</table>

## -remarks

This method calls <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-loadpolicy">LoadPolicy</a> with the input parameter set to <b>LoadOptionReload</b>.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>
