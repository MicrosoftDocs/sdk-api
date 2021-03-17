---
UID: NF:certenroll.IX509EnrollmentPolicyServer.GetTemplates
title: IX509EnrollmentPolicyServer::GetTemplates (certenroll.h)
description: Retrieves a collection of the templates supported by the certificate enrollment policy (CEP) server.
helpviewer_keywords: ["GetTemplates","GetTemplates method [Security]","GetTemplates method [Security]","IX509EnrollmentPolicyServer interface","IX509EnrollmentPolicyServer interface [Security]","GetTemplates method","IX509EnrollmentPolicyServer.GetTemplates","IX509EnrollmentPolicyServer::GetTemplates","certenroll/IX509EnrollmentPolicyServer::GetTemplates","security.ix509enrollmentpolicyserver_gettemplates"]
old-location: security\ix509enrollmentpolicyserver_gettemplates.htm
tech.root: security
ms.assetid: 52dd85aa-033b-43ab-9b71-1080f969bebc
ms.date: 12/05/2018
ms.keywords: GetTemplates, GetTemplates method [Security], GetTemplates method [Security],IX509EnrollmentPolicyServer interface, IX509EnrollmentPolicyServer interface [Security],GetTemplates method, IX509EnrollmentPolicyServer.GetTemplates, IX509EnrollmentPolicyServer::GetTemplates, certenroll/IX509EnrollmentPolicyServer::GetTemplates, security.ix509enrollmentpolicyserver_gettemplates
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
 - IX509EnrollmentPolicyServer::GetTemplates
 - certenroll/IX509EnrollmentPolicyServer::GetTemplates
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
 - IX509EnrollmentPolicyServer.GetTemplates
---

# IX509EnrollmentPolicyServer::GetTemplates


## -description

The <b>GetTemplates</b> method retrieves a collection of the templates supported by the certificate enrollment policy (CEP) server.

## -parameters

### -param pTemplates [out, retval]

Address of a variable that receives a pointer to an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplates">IX509CertificateTemplates</a> interface that represents the template collection.

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