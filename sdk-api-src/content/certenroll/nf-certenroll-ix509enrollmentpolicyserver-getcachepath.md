---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetCachePath
title: IX509EnrollmentPolicyServer::GetCachePath (certenroll.h)
description: Retrieves the path of the policy cache file on the certificate enrollment policy (CEP) server.
helpviewer_keywords: ["GetCachePath","GetCachePath method [Security]","GetCachePath method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetCachePath method","IX509EnrollmentPolicyServer.GetCachePath","IX509EnrollmentPolicyServer::GetCachePath","certenroll/IX509EnrollmentPolicyServer::GetCachePath","security.ix509enrollmentpolicyserver_getcachepath"]
old-location: security\ix509enrollmentpolicyserver_getcachepath.htm
tech.root: security
ms.assetid: c71c9f97-a312-4260-995b-454de6a38cce
ms.date: 12/05/2018
ms.keywords: GetCachePath, GetCachePath method [Security], GetCachePath method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetCachePath method, IX509EnrollmentPolicyServer.GetCachePath, IX509EnrollmentPolicyServer::GetCachePath, certenroll/IX509EnrollmentPolicyServer::GetCachePath, security.ix509enrollmentpolicyserver_getcachepath
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
 - IX509EnrollmentPolicyServer::GetCachePath
 - certenroll/IX509EnrollmentPolicyServer::GetCachePath
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
 - IX509EnrollmentPolicyServer.GetCachePath
---

# IX509EnrollmentPolicyServer::GetCachePath


## -description

The <b>GetCachePath</b> method retrieves the path of the policy cache file on the certificate enrollment policy (CEP) server.

## -parameters

### -param pValue [out, retval]

Pointer to a <b>BSTR</b> that receives the path.

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
The cache path could not be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pValue</i> parameter must not be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> has not been initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>