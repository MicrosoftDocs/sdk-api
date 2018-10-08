---
UID: NS:iketypes.IKEEXT_CERTIFICATE_CREDENTIAL0_
title: IKEEXT_CERTIFICATE_CREDENTIAL0_
author: windows-sdk-content
description: Is used to store credential information specific to certificate authentication.
old-location: fwp\ikeext_certificate_credential0.htm
tech.root: fwp
ms.assetid: 926a7e74-a225-4234-8be0-c8731840756a
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IKEEXT_CERTIFICATE_CREDENTIAL0, IKEEXT_CERTIFICATE_CREDENTIAL0 structure [Filtering], IKEEXT_CERTIFICATE_CREDENTIAL0_, IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT, fwp.ikeext_certificate_credential0, iketypes/IKEEXT_CERTIFICATE_CREDENTIAL0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Iketypes.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iketypes.h
api_name:
 - IKEEXT_CERTIFICATE_CREDENTIAL0
product: Windows
targetos: Windows
req.typenames: IKEEXT_CERTIFICATE_CREDENTIAL0
req.redist: 
---

# IKEEXT_CERTIFICATE_CREDENTIAL0_ structure


## -description


The <b>IKEEXT_CERTIFICATE_CREDENTIAL0</b> structure is used to store credential information specific to certificate authentication.
<div class="alert"><b>Note</b>  <b>IKEEXT_CERTIFICATE_CREDENTIAL0</b> is the specific implementation of IKEEXT_CERTIFICATE_CREDENTIAL used in Windows Vista. See <a href="https://msdn.microsoft.com/FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670">WFP Version-Independent Names and Targeting Specific Versions of Windows</a> for more information. For Windows 7 and later, <a href="https://msdn.microsoft.com/78ae9cfe-2a4f-48cd-9a4f-fd5193df0ed0">IKEEXT_CERTIFICATE_CREDENTIAL1</a> is available.</div><div> </div>

## -struct-fields




### -field subjectName

Encoded subject name of the certificate used for authentication.

See <a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a> for more information.


### -field certHash

SHA thumbprint of the certificate.

See <a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a> for more information.


### -field flags

Possible values:

<a id="IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT"></a>
<a id="ikeext_cert_credential_flag_nap_cert"></a>


#### IKEEXT_CERT_CREDENTIAL_FLAG_NAP_CERT


## -see-also




<a href="https://msdn.microsoft.com/e957132f-417b-40c1-afe3-5aec0e2192f7">Windows Filtering Platform  API Structures</a>
 

 

