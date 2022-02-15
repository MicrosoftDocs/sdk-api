---
UID: NE:tapi3if.TAPI_TONEMODE
title: TAPI_TONEMODE (tapi3if.h)
description: The TAPI_TONEMODE enum is used to describe the different selections that are used when generating line tones.
helpviewer_keywords: ["TAPI_TONEMODE","TAPI_TONEMODE enumeration [TAPI 2.2]","TTM_BEEP","TTM_BILLING","TTM_BUSY","TTM_RINGBACK","_tapi3_tapi_tonemode","tapi3.tapi_tonemode","tapi3if/TAPI_TONEMODE","tapi3if/TTM_BEEP","tapi3if/TTM_BILLING","tapi3if/TTM_BUSY","tapi3if/TTM_RINGBACK"]
old-location: tapi3\tapi_tonemode.htm
tech.root: tapi3
ms.assetid: eeae9d4a-824c-4316-8eb3-846563ac4a54
ms.date: 12/05/2018
ms.keywords: TAPI_TONEMODE, TAPI_TONEMODE enumeration [TAPI 2.2], TTM_BEEP, TTM_BILLING, TTM_BUSY, TTM_RINGBACK, _tapi3_tapi_tonemode, tapi3.tapi_tonemode, tapi3if/TAPI_TONEMODE, tapi3if/TTM_BEEP, tapi3if/TTM_BILLING, tapi3if/TTM_BUSY, tapi3if/TTM_RINGBACK
req.header: tapi3if.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TAPI_TONEMODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TAPI_TONEMODE
 - tapi3if/TAPI_TONEMODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi3if.h
api_name:
 - TAPI_TONEMODE
---

# TAPI_TONEMODE enumeration


## -description

The <b>TAPI_TONEMODE</b> enum is used to describe the different selections that are used when generating line tones.

## -enum-fields

### -field TTM_RINGBACK:0x2

The tone is a ringback tone. Exact definition is service-provider defined.

### -field TTM_BUSY:0x4

The tone is a busy tone. Exact definition is service-provider defined.

### -field TTM_BEEP:0x8

The tone is a beep, such as that used to announce the beginning of a recording. Exact definition is service-provider defined.

### -field TTM_BILLING:0x10

The tone is a billing information tone, such as a credit card prompt tone. Exact definition is service-provider defined.

## -see-also

<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itlegacycallmediacontrol2-generatetone">ITLegacyCallMediaControl2::GenerateTone</a>
