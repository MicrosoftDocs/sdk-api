---
UID: NE:certenroll.PFXExportOptions
title: PFXExportOptions
author: windows-sdk-content
description: Specifies how much of a certificate chain is included when creating a Personal Information Exchange (PFX) message.
old-location: security\pfxexportoptions_enum.htm
old-project: SecCertEnroll
ms.assetid: 72a3ac43-aebf-4801-9e36-23cf338b18ab
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PFXExportChainNoRoot, PFXExportChainWithRoot, PFXExportEEOnly, PFXExportOptions, PFXExportOptions enumeration [Security], certenroll/PFXExportChainNoRoot, certenroll/PFXExportChainWithRoot, certenroll/PFXExportEEOnly, certenroll/PFXExportOptions, security.pfxexportoptions_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PFXExportOptions
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - PFXExportOptions
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# PFXExportOptions enumeration


## -description


The <b>PFXExportOptions</b> enumeration specifies how much of a certificate chain is included when creating a Personal Information Exchange (PFX) message. The PFX message syntax is defined by the PKCS #12 standard. PFX is a transfer syntax for personal identity information, including <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private keys</a> and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificates</a>. The enumeration is used by the <a href="https://msdn.microsoft.com/4a51bea0-e7f8-4a4e-b612-95616b126466">CreatePFX</a> method on the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> interface.


## -enum-fields




### -field PFXExportEEOnly

Includes only the end entity certificate.


### -field PFXExportChainNoRoot

Includes the certificate chain without the root <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> certificate.


### -field PFXExportChainWithRoot

Includes the entire certificate chain, including the root certification authority certificate.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/4a51bea0-e7f8-4a4e-b612-95616b126466">CreatePFX</a>
 

 

