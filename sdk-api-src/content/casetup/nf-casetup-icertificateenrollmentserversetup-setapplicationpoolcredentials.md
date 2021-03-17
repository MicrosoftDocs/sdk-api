---
UID: NF:casetup.ICertificateEnrollmentServerSetup.SetApplicationPoolCredentials
title: ICertificateEnrollmentServerSetup::SetApplicationPoolCredentials (casetup.h)
description: Specifies user account information for the application pool in which the Certificate Enrollment Web Service (CES) runs.
helpviewer_keywords: ["ICertificateEnrollmentServerSetup interface [Security]","SetApplicationPoolCredentials method","ICertificateEnrollmentServerSetup.SetApplicationPoolCredentials","ICertificateEnrollmentServerSetup::SetApplicationPoolCredentials","SetApplicationPoolCredentials","SetApplicationPoolCredentials method [Security]","SetApplicationPoolCredentials method [Security]","ICertificateEnrollmentServerSetup interface","casetup/ICertificateEnrollmentServerSetup::SetApplicationPoolCredentials","security.icertificateenrollmentserversetup_setapplicationpoolcredentials"]
old-location: security\icertificateenrollmentserversetup_setapplicationpoolcredentials.htm
tech.root: security
ms.assetid: E85DA115-C705-44B8-B4D4-E862634CDC41
ms.date: 12/05/2018
ms.keywords: ICertificateEnrollmentServerSetup interface [Security],SetApplicationPoolCredentials method, ICertificateEnrollmentServerSetup.SetApplicationPoolCredentials, ICertificateEnrollmentServerSetup::SetApplicationPoolCredentials, SetApplicationPoolCredentials, SetApplicationPoolCredentials method [Security], SetApplicationPoolCredentials method [Security],ICertificateEnrollmentServerSetup interface, casetup/ICertificateEnrollmentServerSetup::SetApplicationPoolCredentials, security.icertificateenrollmentserversetup_setapplicationpoolcredentials
req.header: casetup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Casetup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Certocm.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertificateEnrollmentServerSetup::SetApplicationPoolCredentials
 - casetup/ICertificateEnrollmentServerSetup::SetApplicationPoolCredentials
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Certocm.dll
api_name:
 - ICertificateEnrollmentServerSetup.SetApplicationPoolCredentials
---

# ICertificateEnrollmentServerSetup::SetApplicationPoolCredentials


## -description

The <b>SetApplicationPoolCredentials</b> method specifies user account information for the application pool in which the Certificate Enrollment Web Service (CES) runs.

## -parameters

### -param bstrUsername [in]

A <b>BSTR</b> that contains the username for the account.

### -param bstrPassword [in]

A <b>BSTR</b> that contains the account password.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>bstrUsername</i> and <i>bstrPassword</i> arguments cannot be <b>NULL</b> or empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a> object has not been initialized.

The <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-get_errorstring">ErrorString</a> property value is set to "The setup object has not been initialized. Please initialize the setup object with the InitializeInstallDefaults method."

</td>
</tr>
</table>

## -remarks

The <b>SetApplicationPoolCredentials</b> method determines whether the user credentials are valid and whether the account is a member of the IIS_IUSRS group. If an error is encountered, the <a href="/windows/desktop/api/casetup/nf-casetup-icertificateenrollmentserversetup-get_errorstring">ErrorString</a> property can be set to any of the following:<ul>
<li>"Setup is unable to obtain security information for the account."</li>
<li>"Setup is unable to check the membership of the account."</li>
<li>"The account is not a member of the local machine's IIS_IUSRS group."</li>
<li>"Fail to retrieve the DNS name of the computer."</li>
<li>"The account should be a domain account.  Local account is not allowed."</li>
</ul>

## -see-also

<a href="/windows/desktop/api/casetup/nn-casetup-icertificateenrollmentserversetup">ICertificateEnrollmentServerSetup</a>