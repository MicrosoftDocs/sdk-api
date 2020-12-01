---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetCAs
title: IX509EnrollmentPolicyServer::GetCAs (certenroll.h)
description: Retrieves a collection of certification enrollment servers included in the policy.
helpviewer_keywords: ["GetCAs","GetCAs method [Security]","GetCAs method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetCAs method","IX509EnrollmentPolicyServer.GetCAs","IX509EnrollmentPolicyServer::GetCAs","certenroll/IX509EnrollmentPolicyServer::GetCAs","security.ix509enrollmentpolicyserver_getcas"]
old-location: security\ix509enrollmentpolicyserver_getcas.htm
tech.root: security
ms.assetid: 37836fd1-e95a-4025-b268-f78a9113e568
ms.date: 12/05/2018
ms.keywords: GetCAs, GetCAs method [Security], GetCAs method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetCAs method, IX509EnrollmentPolicyServer.GetCAs, IX509EnrollmentPolicyServer::GetCAs, certenroll/IX509EnrollmentPolicyServer::GetCAs, security.ix509enrollmentpolicyserver_getcas
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
 - IX509EnrollmentPolicyServer::GetCAs
 - certenroll/IX509EnrollmentPolicyServer::GetCAs
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
 - IX509EnrollmentPolicyServer.GetCAs
---

# IX509EnrollmentPolicyServer::GetCAs


## -description

The <b>GetCAs</b> method retrieves a collection of certification enrollment servers included in the policy.

## -parameters

### -param ppCAs [out, retval]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-icertificationauthorities">ICertificationAuthorities</a> interface that represents the collection.

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
<dt><b>OLE_E_BLANK</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a> object has not been initialized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>