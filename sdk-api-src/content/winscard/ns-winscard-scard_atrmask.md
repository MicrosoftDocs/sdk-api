---
UID: NS:winscard._SCARD_ATRMASK
title: SCARD_ATRMASK (winscard.h)
description: Used by the SCardLocateCardsByATR function to locate cards.
helpviewer_keywords: ["*LPSCARD_ATRMASK","*PSCARD_ATRMASK","LPSCARD_ATRMASK","LPSCARD_ATRMASK structure pointer [Security]","PSCARD_ATRMASK","PSCARD_ATRMASK structure pointer [Security]","SCARD_ATRMASK","SCARD_ATRMASK structure [Security]","_smart_scard_atrmask","security.scard_atrmask","winscard/LPSCARD_ATRMASK","winscard/PSCARD_ATRMASK","winscard/SCARD_ATRMASK"]
old-location: security\scard_atrmask.htm
tech.root: security
ms.assetid: d7f1a747-a858-4bf6-874a-d76aa4227cd2
ms.date: 12/05/2018
ms.keywords: '*LPSCARD_ATRMASK, *PSCARD_ATRMASK, LPSCARD_ATRMASK, LPSCARD_ATRMASK structure pointer [Security], PSCARD_ATRMASK, PSCARD_ATRMASK structure pointer [Security], SCARD_ATRMASK, SCARD_ATRMASK structure [Security], _smart_scard_atrmask, security.scard_atrmask, winscard/LPSCARD_ATRMASK, winscard/PSCARD_ATRMASK, winscard/SCARD_ATRMASK'
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SCARD_ATRMASK
 - winscard/_SCARD_ATRMASK
 - PSCARD_ATRMASK
 - winscard/PSCARD_ATRMASK
 - SCARD_ATRMASK
 - winscard/SCARD_ATRMASK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winscard.h
api_name:
 - SCARD_ATRMASK
---

# SCARD_ATRMASK structure


## -description

The <b>SCARD_ATRMASK</b> structure is used by 
the <a href="/windows/desktop/api/winscard/nf-winscard-scardlocatecardsbyatra">SCardLocateCardsByATR</a> function to locate cards.

## -struct-fields

### -field cbAtr

The number of bytes in the ATR and the mask.

### -field rgbAtr

An array of <b>BYTE</b> values for the ATR of the card with extra alignment bytes.

### -field rgbMask

An array of <b>BYTE</b> values for the mask for the ATR with extra alignment bytes.