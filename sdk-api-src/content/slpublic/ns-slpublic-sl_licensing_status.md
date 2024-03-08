---
UID: NS:slpublic._tagSL_LICENSING_STATUS
title: SL_LICENSING_STATUS (slpublic.h)
description: Represents the licensing status. (SL_LICENSING_STATUS)
helpviewer_keywords: ["SL_LICENSING_STATUS","SL_LICENSING_STATUS structure [Security]","security.sl_licensing_status","slpublic/SL_LICENSING_STATUS"]
old-location: security\sl_licensing_status.htm
tech.root: security
ms.assetid: e7c857d9-6f63-4b1c-a562-abb158914a7d
ms.date: 12/05/2018
ms.keywords: SL_LICENSING_STATUS, SL_LICENSING_STATUS structure [Security], security.sl_licensing_status, slpublic/SL_LICENSING_STATUS
req.header: slpublic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: SL_LICENSING_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _tagSL_LICENSING_STATUS
 - slpublic/_tagSL_LICENSING_STATUS
 - SL_LICENSING_STATUS
 - slpublic/SL_LICENSING_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - slpublic.h
api_name:
 - SL_LICENSING_STATUS
---

# SL_LICENSING_STATUS structure


## -description

Represents the licensing status.

## -struct-fields

### -field SkuId

Type: <b>SLID</b>

The SKU ID.

### -field eStatus

Type: <b><a href="/windows/desktop/api/slpublic/ne-slpublic-sllicensingstatus">SLLICENSINGSTATUS</a></b>

The licensing status.

### -field dwGraceTime

Type: <b>DWORD</b>

The grace time in minutes.

### -field dwTotalGraceDays

Type: <b>DWORD</b>

The predefined grace days in the license.

### -field hrReason

Type: <b>HRESULT</b>

The error of unlicensed status.

### -field qwValidityExpiration

Type: <b>UINT64</b>

The validity expiration day.
