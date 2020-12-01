---
UID: NS:iketypes.IKEEXT_CERT_EKUS0_
title: IKEEXT_CERT_EKUS0 (iketypes.h)
description: Contains information about the extended key usage (EKU) properties of a certificate.
helpviewer_keywords: ["IKEEXT_CERT_EKUS0","IKEEXT_CERT_EKUS0 structure [Filtering]","fwp.ikeext_cert_ekus0","iketypes/IKEEXT_CERT_EKUS0"]
old-location: fwp\ikeext_cert_ekus0.htm
tech.root: fwp
ms.assetid: e9669340-a1f2-455f-a490-a94694c83531
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERT_EKUS0, IKEEXT_CERT_EKUS0 structure [Filtering], fwp.ikeext_cert_ekus0, iketypes/IKEEXT_CERT_EKUS0
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
targetos: Windows
req.typenames: IKEEXT_CERT_EKUS0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CERT_EKUS0_
 - iketypes/IKEEXT_CERT_EKUS0_
 - IKEEXT_CERT_EKUS0
 - iketypes/IKEEXT_CERT_EKUS0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - iketypes.h
api_name:
 - IKEEXT_CERT_EKUS0
---

# IKEEXT_CERT_EKUS0 structure


## -description

The <b>IKEEXT_CERT_EKUS0</b> structure contains information about the extended key usage (EKU) properties of a certificate.

## -struct-fields

### -field numEku

Type: <b>ULONG</b>

 The number of EKUs in the <b>eku</b> member.

### -field eku

Type: <b>LPSTR*</b>

The list of EKU object identifiers (OIDs).

