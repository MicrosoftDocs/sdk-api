---
UID: NS:iketypes.IKEEXT_CERT_NAME0_
title: IKEEXT_CERT_NAME0 (iketypes.h)
description: Specifies certificate selection &quot;subject&quot; criteria for an authentication method.
helpviewer_keywords: ["IKEEXT_CERT_NAME0","IKEEXT_CERT_NAME0 structure [Filtering]","fwp.ikeext_cert_name0","iketypes/IKEEXT_CERT_NAME0"]
old-location: fwp\ikeext_cert_name0.htm
tech.root: fwp
ms.assetid: 50e04e10-cae1-4fcd-990e-3e9b538627ed
ms.date: 12/05/2018
ms.keywords: IKEEXT_CERT_NAME0, IKEEXT_CERT_NAME0 structure [Filtering], fwp.ikeext_cert_name0, iketypes/IKEEXT_CERT_NAME0
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
req.typenames: IKEEXT_CERT_NAME0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IKEEXT_CERT_NAME0_
 - iketypes/IKEEXT_CERT_NAME0_
 - IKEEXT_CERT_NAME0
 - iketypes/IKEEXT_CERT_NAME0
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
 - IKEEXT_CERT_NAME0
---

# IKEEXT_CERT_NAME0 structure


## -description

The <b>IKEEXT_CERT_NAME0</b> structure specifies certificate selection "subject" criteria for an authentication method.

## -struct-fields

### -field nameType

Type: [IKEEXT_CERT_CRITERIA_NAME_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)</b>

The type of NAME field.

### -field certName

Type: <b>LPWSTR</b>

The string to be used for matching the "subject" criteria.

## -see-also

[IKEEXT_CERT_CRITERIA_NAME_TYPE](/windows/desktop/api/iketypes/ne-iketypes-ikeext_cert_criteria_name_type)