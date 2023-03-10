---
UID: NS:wincrypt._CTL_VERIFY_USAGE_STATUS
title: CTL_VERIFY_USAGE_STATUS (wincrypt.h)
description: Contains information about a Certificate Trust List (CTL) returned by CertVerifyCTLUsage.
helpviewer_keywords: ["*PCTL_VERIFY_USAGE_STATUS","CTL_VERIFY_USAGE_STATUS","CTL_VERIFY_USAGE_STATUS structure [Security]","PCTL_VERIFY_USAGE_STATUS","PCTL_VERIFY_USAGE_STATUS structure pointer [Security]","_crypto2_ctl_verify_usage_status","security.ctl_verify_usage_status","wincrypt/CTL_VERIFY_USAGE_STATUS","wincrypt/PCTL_VERIFY_USAGE_STATUS"]
old-location: security\ctl_verify_usage_status.htm
tech.root: security
ms.assetid: 2b7ef953-9422-4dcf-b293-a78a06bb080e
ms.date: 12/05/2018
ms.keywords: '*PCTL_VERIFY_USAGE_STATUS, CTL_VERIFY_USAGE_STATUS, CTL_VERIFY_USAGE_STATUS structure [Security], PCTL_VERIFY_USAGE_STATUS, PCTL_VERIFY_USAGE_STATUS structure pointer [Security], _crypto2_ctl_verify_usage_status, security.ctl_verify_usage_status, wincrypt/CTL_VERIFY_USAGE_STATUS, wincrypt/PCTL_VERIFY_USAGE_STATUS'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: CTL_VERIFY_USAGE_STATUS, *PCTL_VERIFY_USAGE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CTL_VERIFY_USAGE_STATUS
 - wincrypt/_CTL_VERIFY_USAGE_STATUS
 - PCTL_VERIFY_USAGE_STATUS
 - wincrypt/PCTL_VERIFY_USAGE_STATUS
 - CTL_VERIFY_USAGE_STATUS
 - wincrypt/CTL_VERIFY_USAGE_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CTL_VERIFY_USAGE_STATUS
---

# CTL_VERIFY_USAGE_STATUS structure


## -description

The <b>CTL_VERIFY_USAGE_STATUS</b> structure contains information about a <a href="/windows/desktop/SecGloss/c-gly">Certificate Trust List</a> (CTL) returned by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyctlusage">CertVerifyCTLUsage</a>.

## -struct-fields

### -field cbSize

The size, in bytes, of the structure. The application calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyctlusage">CertVerifyCTLUsage</a> sets this parameter. If <b>cbSize</b> is not greater than or equal to the required size of the structure, <b>CertVerifyCTLUsage</b> returns <b>FALSE</b> and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>E_INVALIDARG</b>.

### -field dwError

The error status, if any, returned by the call to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyctlusage">CertVerifyCTLUsage</a>. For the list of possible error values, see the Return Values section in <b>CertVerifyCTLUsage</b>.

### -field dwFlags

If <b>CERT_VERIFY_UPDATED_CTL_FLAG</b> is returned, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyctlusage">CertVerifyCTLUsage</a> updated a CTL whose time was no longer valid with a new, time-valid CTL.

### -field ppCtl

Pointer to a pointer to a CTL <a href="/windows/desktop/SecGloss/c-gly">context</a> containing the matched subject. The calling application can set this pointer to <b>NULL</b> to indicate that a CTL containing the subject is not to be returned. 




If <b>ppCtl</b> is not <b>NULL</b>, the calling application must free the returned context using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>.

### -field dwCtlEntryIndex

Returns the array location of the matching subject's entry in the CTL's array.

### -field ppSigner

A pointer to a pointer to the certificate context of the signer of the CTL. This pointer can be set to <b>NULL</b> by the calling application indicating that the certificate of the signer of the CTL is not to be returned. 




If <b>ppSigner</b> is not <b>NULL</b>, the calling application must free the returned context using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>.

### -field dwSignerIndex

Index of the signer actually used. Needed if a message has more than one signer.

## -remarks

The members <b>dwError</b>, <b>dwFlags</b>, <b>dwCtlEntryIndex</b>, and <b>dwSignerIndex</b> should be initialized to zero by the calling application.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certverifyctlusage">CertVerifyCTLUsage</a>