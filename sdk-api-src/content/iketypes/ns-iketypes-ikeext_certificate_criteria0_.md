---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IKEEXT_CERTIFICATE_CRITERIA0_ structure


## -description


The <b>IKEEXT_CERTIFICATE_CRITERIA0</b> structure contains a set of criteria to applied to an authentication method.


## -struct-fields




### -field certData

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a></b>

X509/ASN.1 encoded name of the root certificate. Should be empty when
   specifying Enterprise or trusted root store config.


### -field certHash

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a></b>

  16-character hexadecimal string that represents the ID, thumbprint or HASH of the end certificate.


### -field eku

Type: <b><a href="https://msdn.microsoft.com/e9669340-a1f2-455f-a490-a94694c83531">IKEEXT_CERT_EKUS0</a>*</b>

The specific extended key usage (EKU) object identifiers (OIDs) selected for the criteria on the end certificate.


### -field name

Type: <b><a href="https://msdn.microsoft.com/50e04e10-cae1-4fcd-990e-3e9b538627ed">IKEEXT_CERT_NAME0</a>*</b>

The name/subject selected for the criteria on the end certificate.


### -field flags

Type: <b>UINT32</b>

Reserved for system use.


## -remarks



The <b>certData</b> member refers to the encoded name of the root certificate, while the <b>certHash</b>, <b>eku</b>, and <b>name</b> members refer to criteria on the end certificate.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff552427">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/e9669340-a1f2-455f-a490-a94694c83531">IKEEXT_CERT_EKUS0</a>



<a href="https://msdn.microsoft.com/50e04e10-cae1-4fcd-990e-3e9b538627ed">IKEEXT_CERT_NAME0</a>
 

 

