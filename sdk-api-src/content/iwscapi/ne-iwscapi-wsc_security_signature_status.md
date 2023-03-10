---
UID: NE:iwscapi._WSC_SECURITY_SIGNATURE_STATUS
title: WSC_SECURITY_SIGNATURE_STATUS (iwscapi.h)
description: Reports the current version status of the security product to Windows Security Center.
helpviewer_keywords: ["WSC_SECURITY_PRODUCT_OUT_OF_DATE","WSC_SECURITY_PRODUCT_UP_TO_DATE","WSC_SECURITY_SIGNATURE_STATUS","WSC_SECURITY_SIGNATURE_STATUS enumeration [Windows API]","iwscapi/WSC_SECURITY_PRODUCT_OUT_OF_DATE","iwscapi/WSC_SECURITY_PRODUCT_UP_TO_DATE","iwscapi/WSC_SECURITY_SIGNATURE_STATUS","winprog.wsc_security_signature_status"]
old-location: winprog\wsc_security_signature_status.htm
tech.root: winprog
ms.assetid: 1D09F5C6-F5A4-40A5-836B-25709E3017B9
ms.date: 12/05/2018
ms.keywords: WSC_SECURITY_PRODUCT_OUT_OF_DATE, WSC_SECURITY_PRODUCT_UP_TO_DATE, WSC_SECURITY_SIGNATURE_STATUS, WSC_SECURITY_SIGNATURE_STATUS enumeration [Windows API], iwscapi/WSC_SECURITY_PRODUCT_OUT_OF_DATE, iwscapi/WSC_SECURITY_PRODUCT_UP_TO_DATE, iwscapi/WSC_SECURITY_SIGNATURE_STATUS, winprog.wsc_security_signature_status
req.header: iwscapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wscapi.lib
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: WSC_SECURITY_SIGNATURE_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WSC_SECURITY_SIGNATURE_STATUS
 - iwscapi/_WSC_SECURITY_SIGNATURE_STATUS
 - WSC_SECURITY_SIGNATURE_STATUS
 - iwscapi/WSC_SECURITY_SIGNATURE_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - Wscapi.lib
api_name:
 - WSC_SECURITY_SIGNATURE_STATUS
---

# WSC_SECURITY_SIGNATURE_STATUS enumeration


## -description

Reports the current version  status of the security product to Windows Security Center.

## -enum-fields

### -field WSC_SECURITY_PRODUCT_OUT_OF_DATE:0

The security software reports that it is not the most recent version.

### -field WSC_SECURITY_PRODUCT_UP_TO_DATE:1

The security software reports that it is the most recent version.

