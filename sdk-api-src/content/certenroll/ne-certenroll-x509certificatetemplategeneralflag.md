---
UID: NE:certenroll.X509CertificateTemplateGeneralFlag
title: X509CertificateTemplateGeneralFlag (certenroll.h)
description: Contains use and modification information about templates and associated certificates.
helpviewer_keywords: ["GeneralCA","GeneralCrossCA","GeneralDefault","GeneralDonotPersist","GeneralMachineType","GeneralModified","X509CertificateTemplateGeneralFlag","X509CertificateTemplateGeneralFlag enumeration [Security]","certenroll/GeneralCA","certenroll/GeneralCrossCA","certenroll/GeneralDefault","certenroll/GeneralDonotPersist","certenroll/GeneralMachineType","certenroll/GeneralModified","certenroll/X509CertificateTemplateGeneralFlag","security.x509certificatetemplategeneralflag"]
old-location: security\x509certificatetemplategeneralflag.htm
tech.root: security
ms.assetid: 0211dd53-39b7-49fb-8acd-e4d02a226904
ms.date: 12/05/2018
ms.keywords: GeneralCA, GeneralCrossCA, GeneralDefault, GeneralDonotPersist, GeneralMachineType, GeneralModified, X509CertificateTemplateGeneralFlag, X509CertificateTemplateGeneralFlag enumeration [Security], certenroll/GeneralCA, certenroll/GeneralCrossCA, certenroll/GeneralDefault, certenroll/GeneralDonotPersist, certenroll/GeneralMachineType, certenroll/GeneralModified, certenroll/X509CertificateTemplateGeneralFlag, security.x509certificatetemplategeneralflag
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: X509CertificateTemplateGeneralFlag
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X509CertificateTemplateGeneralFlag
 - certenroll/X509CertificateTemplateGeneralFlag
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
 - X509CertificateTemplateGeneralFlag
---

# X509CertificateTemplateGeneralFlag enumeration


## -description

The <b>X509CertificateTemplateGeneralFlag</b> enumeration contains use and modification information about templates and associated certificates.

## -enum-fields

### -field GeneralMachineType:0x40

The template should be used to create a certificate request for a computer.

### -field GeneralCA:0x80

The template should be used to create a request for a certification authority certificate.

### -field GeneralCrossCA:0x800

The template should be used to create a request to cross certify a certificate.

### -field GeneralDefault:0x10000

The template is not used by the client or server in the Windows Client Certificate Enrollment and should not be modified.

### -field GeneralModified:0x20000

The template is not used by the client or server in the Windows Client Certificate Enrollment and can be modified if necessary.

### -field GeneralDonotPersist:0x1000

The certification authority is not required to save a record of a certificate request for a certificate that has been issued.

