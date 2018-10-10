---
UID: NS:iketypes.IKEEXT_CERTIFICATE_CRITERIA0_
title: IKEEXT_CERTIFICATE_CRITERIA0_
author: windows-sdk-content
description: Contains a set of criteria to applied to an authentication method.
old-location: fwp\ikeext_certificate_criteria0.htm
tech.root: FWP
ms.assetid: dbcb0e25-fdde-44d9-bfad-b3605f563773
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: IKEEXT_CERTIFICATE_CRITERIA0, IKEEXT_CERTIFICATE_CRITERIA0 structure [Filtering], IKEEXT_CERTIFICATE_CRITERIA0_, fwp.ikeext_certificate_criteria0, iketypes/IKEEXT_CERTIFICATE_CRITERIA0
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: iketypes.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - iketypes.h
api_name:
 - IKEEXT_CERTIFICATE_CRITERIA0
product: Windows
targetos: Windows
req.typenames: IKEEXT_CERTIFICATE_CRITERIA0
req.redist: 
---

# IKEEXT_CERTIFICATE_CRITERIA0_ structure


## -description


The <b>IKEEXT_CERTIFICATE_CRITERIA0</b> structure contains a set of criteria to applied to an authentication method.


## -struct-fields




### -field certData

Type: <b><a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a></b>

X509/ASN.1 encoded name of the root certificate. Should be empty when
   specifying Enterprise or trusted root store config.


### -field certHash

Type: <b><a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a></b>

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




<a href="https://msdn.microsoft.com/85f360bf-5ee4-4980-b4ce-15ff310d8fbe">FWP_BYTE_BLOB</a>



<a href="https://msdn.microsoft.com/e9669340-a1f2-455f-a490-a94694c83531">IKEEXT_CERT_EKUS0</a>



<a href="https://msdn.microsoft.com/50e04e10-cae1-4fcd-990e-3e9b538627ed">IKEEXT_CERT_NAME0</a>
 

 

