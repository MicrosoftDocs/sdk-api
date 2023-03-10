---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetCacheDir
title: IX509EnrollmentPolicyServer::GetCacheDir (certenroll.h)
description: Retrieves the name of the directory on the certificate enrollment policy (CEP) server that contains the policy cache file.
helpviewer_keywords: ["GetCacheDir","GetCacheDir method [Security]","GetCacheDir method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetCacheDir method","IX509EnrollmentPolicyServer.GetCacheDir","IX509EnrollmentPolicyServer::GetCacheDir","certenroll/IX509EnrollmentPolicyServer::GetCacheDir","security.ix509enrollmentpolicyserver_getcachedir"]
old-location: security\ix509enrollmentpolicyserver_getcachedir.htm
tech.root: security
ms.assetid: 72b0b6f0-cc4f-4e03-9b6c-7bd4c12cf0a3
ms.date: 12/05/2018
ms.keywords: GetCacheDir, GetCacheDir method [Security], GetCacheDir method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetCacheDir method, IX509EnrollmentPolicyServer.GetCacheDir, IX509EnrollmentPolicyServer::GetCacheDir, certenroll/IX509EnrollmentPolicyServer::GetCacheDir, security.ix509enrollmentpolicyserver_getcachedir
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
 - IX509EnrollmentPolicyServer::GetCacheDir
 - certenroll/IX509EnrollmentPolicyServer::GetCacheDir
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
 - IX509EnrollmentPolicyServer.GetCacheDir
---

# IX509EnrollmentPolicyServer::GetCacheDir


## -description

The <b>GetCacheDir</b> method retrieves the name of the directory on the certificate enrollment policy (CEP) server that contains the policy cache file.

## -parameters

### -param pValue [out, retval]

Pointer to a <b>BSTR</b> that receives the directory name.

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
The cache directory could not be found.

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