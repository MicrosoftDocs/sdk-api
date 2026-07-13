---
UID: NE:certenroll.InstallResponseRestrictionFlags
title: InstallResponseRestrictionFlags (certenroll.h)
description: Contains flags that identify the restrictions placed on the local installation of a certificate chain.
helpviewer_keywords: ["AllowNoOutstandingRequest","AllowNone","AllowUntrustedCertificate","AllowUntrustedRoot","InstallResponseRestrictionFlags","InstallResponseRestrictionFlags enumeration [Security]","certenroll/AllowNoOutstandingRequest","certenroll/AllowNone","certenroll/AllowUntrustedCertificate","certenroll/AllowUntrustedRoot","certenroll/InstallResponseRestrictionFlags","security.installresponserestrictionflags_enum"]
old-location: security\installresponserestrictionflags_enum.htm
tech.root: security
ms.assetid: 070cadd8-08cf-44ce-a8b7-39a4fb11e724
ms.date: 12/05/2018
ms.keywords: AllowNoOutstandingRequest, AllowNone, AllowUntrustedCertificate, AllowUntrustedRoot, InstallResponseRestrictionFlags, InstallResponseRestrictionFlags enumeration [Security], certenroll/AllowNoOutstandingRequest, certenroll/AllowNone, certenroll/AllowUntrustedCertificate, certenroll/AllowUntrustedRoot, certenroll/InstallResponseRestrictionFlags, security.installresponserestrictionflags_enum
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: InstallResponseRestrictionFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InstallResponseRestrictionFlags
 - certenroll/InstallResponseRestrictionFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - InstallResponseRestrictionFlags
---

# InstallResponseRestrictionFlags enumeration


## -description

The <b>InstallResponseRestrictionFlags</b> enumeration contains flags that identify the restrictions placed on the local installation of a certificate chain. This enumeration is used by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-installresponse">InstallResponse</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface.

## -enum-fields

### -field AllowNone:0

Does not allow the installation of untrusted certificates or certificates for which there is no corresponding request.

### -field AllowNoOutstandingRequest:0x1

Creates the <a href="/windows/desktop/SecGloss/p-gly">private key</a> from the certificate response rather than from the dummy certificate. This makes the dummy certificate optional. If this value is not set, the dummy certificate must exist, and the private key is extracted from it.

### -field AllowUntrustedCertificate:0x2

Installs untrusted end entity and <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> certificates. Certification authority certificates include root and subordinate certification authority certificates. End entity certificates are installed to the personal store, and certification authority certificates are installed to the certification authority store.

### -field AllowUntrustedRoot:0x4

Performs the same action as the <b>AllowUntrustedCertificate</b> flag but also installs the certificate even if the certificate chain cannot be built because the root is not trusted.

<div class="alert"><b>Note</b>  On Windows Vista, the behavior of this flag is the same as that defined for the <b>AllowUntrustedCertificate</b> flag. You can install an untrusted root beginning with Windows Vista with SP1.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-installresponse">InstallResponse</a>
