---
UID: NE:certenroll.PFXExportOptions
title: PFXExportOptions (certenroll.h)
description: Specifies how much of a certificate chain is included when creating a Personal Information Exchange (PFX) message.
helpviewer_keywords: ["PFXExportChainNoRoot","PFXExportChainWithRoot","PFXExportEEOnly","PFXExportOptions","PFXExportOptions enumeration [Security]","certenroll/PFXExportChainNoRoot","certenroll/PFXExportChainWithRoot","certenroll/PFXExportEEOnly","certenroll/PFXExportOptions","security.pfxexportoptions_enum"]
old-location: security\pfxexportoptions_enum.htm
tech.root: security
ms.assetid: 72a3ac43-aebf-4801-9e36-23cf338b18ab
ms.date: 12/05/2018
ms.keywords: PFXExportChainNoRoot, PFXExportChainWithRoot, PFXExportEEOnly, PFXExportOptions, PFXExportOptions enumeration [Security], certenroll/PFXExportChainNoRoot, certenroll/PFXExportChainWithRoot, certenroll/PFXExportEEOnly, certenroll/PFXExportOptions, security.pfxexportoptions_enum
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
req.typenames: PFXExportOptions
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFXExportOptions
 - certenroll/PFXExportOptions
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
 - PFXExportOptions
---

# PFXExportOptions enumeration


## -description

The <b>PFXExportOptions</b> enumeration specifies how much of a certificate chain is included when creating a Personal Information Exchange (PFX) message. The PFX message syntax is defined by the PKCS #12 standard. PFX is a transfer syntax for personal identity information, including <a href="/windows/desktop/SecGloss/p-gly">private keys</a> and <a href="/windows/desktop/SecGloss/c-gly">certificates</a>. The enumeration is used by the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-createpfx">CreatePFX</a> method on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509enrollment">IX509Enrollment</a> interface.

## -enum-fields

### -field PFXExportEEOnly:0

Includes only the end entity certificate.

### -field PFXExportChainNoRoot:1

Includes the certificate chain without the root <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> certificate.

### -field PFXExportChainWithRoot:2

Includes the entire certificate chain, including the root certification authority certificate.

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nf-certenroll-ix509enrollment-createpfx">CreatePFX</a>
