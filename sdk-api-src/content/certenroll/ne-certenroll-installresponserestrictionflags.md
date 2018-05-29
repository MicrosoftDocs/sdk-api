---
UID: NE:certenroll.InstallResponseRestrictionFlags
title: InstallResponseRestrictionFlags
author: windows-sdk-content
description: Contains flags that identify the restrictions placed on the local installation of a certificate chain.
old-location: security\installresponserestrictionflags_enum.htm
old-project: SecCertEnroll
ms.assetid: 070cadd8-08cf-44ce-a8b7-39a4fb11e724
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: AllowNoOutstandingRequest, AllowNone, AllowUntrustedCertificate, AllowUntrustedRoot, InstallResponseRestrictionFlags, InstallResponseRestrictionFlags enumeration [Security], certenroll/AllowNoOutstandingRequest, certenroll/AllowNone, certenroll/AllowUntrustedCertificate, certenroll/AllowUntrustedRoot, certenroll/InstallResponseRestrictionFlags, security.installresponserestrictionflags_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
req.typenames: InstallResponseRestrictionFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	CertEnroll.h
api_name:
-	InstallResponseRestrictionFlags
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# InstallResponseRestrictionFlags enumeration


## -description


The <b>InstallResponseRestrictionFlags</b> enumeration contains flags that identify the restrictions placed on the local installation of a certificate chain. This enumeration is used by the <a href="https://msdn.microsoft.com/4ad33092-71c4-4ae1-a3a6-cef376d04c2d">InstallResponse</a> method on the <a href="https://msdn.microsoft.com/37f1dd3b-bbe9-40ab-87c9-2405d97f5541">IX509Enrollment</a> interface.


## -enum-fields




### -field AllowNone

Does not allow the installation of untrusted certificates or certificates for which there is no corresponding request.


### -field AllowNoOutstandingRequest

Creates the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a> from the certificate response rather than from the dummy certificate. This makes the dummy certificate optional. If this value is not set, the dummy certificate must exist, and the private key is extracted from it.


### -field AllowUntrustedCertificate

Installs untrusted end entity and <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> certificates. Certification authority certificates include root and subordinate certification authority certificates. End entity certificates are installed to the personal store, and certification authority certificates are installed to the certification authority store.


### -field AllowUntrustedRoot

Performs the same action as the <b>AllowUntrustedCertificate</b> flag but also installs the certificate even if the certificate chain cannot be built because the root is not trusted.

<div class="alert"><b>Note</b>  On Windows Vista, the behavior of this flag is the same as that defined for the <b>AllowUntrustedCertificate</b> flag. You can install an untrusted root beginning with Windows Vista with SP1.</div>
<div> </div>

## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/4ad33092-71c4-4ae1-a3a6-cef376d04c2d">InstallResponse</a>
 

 

