---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetPolicyServerUrl
title: IX509EnrollmentPolicyServer::GetPolicyServerUrl (certenroll.h)
description: Retrieves a string value that contains the URL for the certificate enrollment policy (CEP) server.
helpviewer_keywords: ["GetPolicyServerUrl","GetPolicyServerUrl method [Security]","GetPolicyServerUrl method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetPolicyServerUrl method","IX509EnrollmentPolicyServer.GetPolicyServerUrl","IX509EnrollmentPolicyServer::GetPolicyServerUrl","certenroll/IX509EnrollmentPolicyServer::GetPolicyServerUrl","security.ix509enrollmentpolicyserver_getpolicyserverurl"]
old-location: security\ix509enrollmentpolicyserver_getpolicyserverurl.htm
tech.root: security
ms.assetid: 34fb1430-afde-43f2-a425-dcb25c9ea58d
ms.date: 12/05/2018
ms.keywords: GetPolicyServerUrl, GetPolicyServerUrl method [Security], GetPolicyServerUrl method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetPolicyServerUrl method, IX509EnrollmentPolicyServer.GetPolicyServerUrl, IX509EnrollmentPolicyServer::GetPolicyServerUrl, certenroll/IX509EnrollmentPolicyServer::GetPolicyServerUrl, security.ix509enrollmentpolicyserver_getpolicyserverurl
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
 - IX509EnrollmentPolicyServer::GetPolicyServerUrl
 - certenroll/IX509EnrollmentPolicyServer::GetPolicyServerUrl
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
 - IX509EnrollmentPolicyServer.GetPolicyServerUrl
---

# IX509EnrollmentPolicyServer::GetPolicyServerUrl


## -description

The <b>GetPolicyServerUrl</b> method retrieves a string value that contains the URL for the certificate enrollment policy (CEP) server. This value is set in the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-initialize">Initialize</a> method.

## -parameters

### -param pValue [out, retval]

Pointer to a <b>BSTR</b> variable that contains the URL.

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
The URL could not be found.

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