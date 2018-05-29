---
UID: NS:iketypes.IKEEXT_CERTIFICATE_CREDENTIAL1_
title: IKEEXT_CERTIFICATE_CREDENTIAL1_
author: windows-sdk-content
description: Is used to store credential information specific to certificate authentication.
old-location: fwp\ikeext_certificate_credential1.htm
old-project: FWP
ms.assetid: 78ae9cfe-2a4f-48cd-9a4f-fd5193df0ed0
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: IKEEXT_CERTIFICATE_CREDENTIAL1, IKEEXT_CERTIFICATE_CREDENTIAL1 structure [Filtering], IKEEXT_CERTIFICATE_CREDENTIAL1_, IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT, fwp.ikeext_certificate_credential1, iketypes/IKEEXT_CERTIFICATE_CREDENTIAL1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: IKEEXT_CERTIFICATE_CREDENTIAL1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Iketypes.h
api_name:
-	IKEEXT_CERTIFICATE_CREDENTIAL1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKEEXT_CERTIFICATE_CREDENTIAL1_ structure


## -description


The <b>IKEEXT_CERTIFICATE_CREDENTIAL1</b> structure is used to store credential information specific to certificate authentication.<div class="alert"><b>Note</b>  <b>IKEEXT_CERTIFICATE_CREDENTIAL1</b> is the specific implementation of IKEEXT_CERTIFICATE_CREDENTIAL used in Windows 7 and later. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows Vista, <a href="https://msdn.microsoft.com/926a7e74-a225-4234-8be0-c8731840756a">IKEEXT_CERTIFICATE_CREDENTIAL0</a> is available.</div>
<div> </div>



## -struct-fields




### -field subjectName

Encoded subject name of the certificate used for authentication. Use <a href="https://msdn.microsoft.com/b3d96de8-5cbc-4ccb-b759-6757520bbda3">CertNameToStr</a> to convert the encoded name to string.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> for more information.


### -field certHash

SHA thumbprint of the certificate.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> for more information.


### -field flags

Possible values:

<a id="IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT"></a>
<a id="ikeext_cert_credential_flag_nap_cert"></a>


#### IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT


### -field certificate

The encoded certificate. Use <a href="https://msdn.microsoft.com/a32714c4-ee88-48a8-a40a-bbbfec0613ac">CertCreateCertificateContext</a> to create a certificate context from the encoded certificate.

See <a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a> for more information.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

