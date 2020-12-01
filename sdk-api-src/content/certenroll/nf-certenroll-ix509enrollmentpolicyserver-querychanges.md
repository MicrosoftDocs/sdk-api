---
UID: NF:certenroll.IX509EnrollmentPolicyServer.QueryChanges
title: IX509EnrollmentPolicyServer::QueryChanges (certenroll.h)
description: Retrieves a value that specifies whether the template or certification authority collections have changed in Active Directory.
helpviewer_keywords: ["IX509EnrollmentPolicyServer interface [Security]","QueryChanges method","IX509EnrollmentPolicyServer.QueryChanges","IX509EnrollmentPolicyServer::QueryChanges","QueryChanges","QueryChanges method [Security]","QueryChanges method [Security]","IX509EnrollmentPolicyServer interface","certenroll/IX509EnrollmentPolicyServer::QueryChanges","security.ix509enrollmentpolicyserver_querychanges"]
old-location: security\ix509enrollmentpolicyserver_querychanges.htm
tech.root: security
ms.assetid: c83faaba-0355-4765-bc08-5e0e02afe8c2
ms.date: 12/05/2018
ms.keywords: IX509EnrollmentPolicyServer interface [Security],QueryChanges method, IX509EnrollmentPolicyServer.QueryChanges, IX509EnrollmentPolicyServer::QueryChanges, QueryChanges, QueryChanges method [Security], QueryChanges method [Security],IX509EnrollmentPolicyServer interface, certenroll/IX509EnrollmentPolicyServer::QueryChanges, security.ix509enrollmentpolicyserver_querychanges
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
 - IX509EnrollmentPolicyServer::QueryChanges
 - certenroll/IX509EnrollmentPolicyServer::QueryChanges
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
 - IX509EnrollmentPolicyServer.QueryChanges
---

# IX509EnrollmentPolicyServer::QueryChanges


## -description

The <b>QueryChanges</b> method retrieves a value that specifies whether the template or certification authority collections have changed in Active Directory.

## -parameters

### -param pValue [out, retval]

Pointer to a Boolean value that specifies whether the collections have changed.

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
LoadOptionRegisterForADChanges was not specified in the <i>option</i> parameter of the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-loadpolicy">LoadPolicy</a> method.

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

## -remarks

The <b>QueryChanges</b> method is relevant only when you specify <b>LoadOptionRegisterForADChanges</b> in the <i>option</i> parameter of the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-loadpolicy">LoadPolicy</a> method. The method returns <b>VARIANT_TRUE</b> for either of the following cases:

<ul>
<li>The template collection in Active Directory has changed since the last time <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-gettemplates">GetTemplates</a> was called.</li>
<li>The certification authority collection in Active Directory has changed since the last time <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollmentpolicyserver-getcas">GetCAs</a> was called.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmentpolicyserver">IX509EnrollmentPolicyServer</a>