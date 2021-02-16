---
UID: NF:certenroll.IX509EnrollmentHelper.Enroll
title: IX509EnrollmentHelper::Enroll (certenroll.h)
description: Enrolls a certificate request and retrieves the issued certificate.
helpviewer_keywords: ["Enroll","Enroll method [Security]","Enroll method [Security]","IX509EnrollmentHelper interface","EnrollPrompt","IX509EnrollmentHelper interface [Security]","Enroll method","IX509EnrollmentHelper.Enroll","IX509EnrollmentHelper::Enroll","certenroll/IX509EnrollmentHelper::Enroll","security.ix509enrollmenthelper_enroll"]
old-location: security\ix509enrollmenthelper_enroll.htm
tech.root: security
ms.assetid: 4f178df7-714f-49e6-9bf5-647acc23b0ad
ms.date: 12/05/2018
ms.keywords: Enroll, Enroll method [Security], Enroll method [Security],IX509EnrollmentHelper interface, EnrollPrompt, IX509EnrollmentHelper interface [Security],Enroll method, IX509EnrollmentHelper.Enroll, IX509EnrollmentHelper::Enroll, certenroll/IX509EnrollmentHelper::Enroll, security.ix509enrollmenthelper_enroll
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
 - IX509EnrollmentHelper::Enroll
 - certenroll/IX509EnrollmentHelper::Enroll
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
 - IX509EnrollmentHelper.Enroll
---

# IX509EnrollmentHelper::Enroll


## -description

The <b>Enroll</b> method enrolls a certificate request and retrieves the issued certificate. This method is web enabled.

## -parameters

### -param strEnrollmentPolicyServerURI [in]

A <b>BSTR</b> that contains the certificate enrollment policy server URL.

### -param strTemplateName [in]

A  <b>BSTR</b> variable that contains the Common Name (CN) of the template as it appears in Active Directory or the dotted decimal <a href="/windows/desktop/SecGloss/o-gly">object identifier</a>.

### -param Encoding [in]

An <a href="/windows/desktop/api/certenroll/ne-certenroll-encodingtype">EncodingType</a> enumeration value that specifies the type of encoding applied to a byte array for display purposes.

### -param enrollFlags [in]

A <a href="/windows/desktop/api/certenroll/ne-certenroll-webenrollmentflags">WebEnrollmentFlags</a> enumeration value that specifies web enrollment behavior. This can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EnrollPrompt"></a><a id="enrollprompt"></a><a id="ENROLLPROMPT"></a><dl>
<dt><b>EnrollPrompt</b></dt>
</dl>
</td>
<td width="60%">
If this flag is set and no authentication credential is available for the certificate enrollment server, the certificate service prompts for a credential. If there is no authentication credential and this flag is not set, the <b>Enroll</b> method fails.

</td>
</tr>
</table>

### -param pstrCertificate [out, retval]

A <b>BSTR</b> that contains the issued certificate.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>strEnrollmentPolicyServerURI</i> and <i>strTemplateName</i> parameters cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_ARITHMETIC_OVERFLOW)</b></dt>
</dl>
</td>
<td width="60%">
The <i>strEnrollmentPolicyServerURI</i> and <i>strTemplateName</i> parameters exceed 64,000 characters or contain embedded null characters.

</td>
</tr>
</table>

## -remarks

The <b>Enroll</b> method retrieves the appropriate template, calls <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment2-initializefromtemplate">InitializeFromTemplate</a>, and then calls <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-enroll">Enroll</a> on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> object.

This method does not installed the issued certificate.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollmenthelper">IX509EnrollmentHelper</a>