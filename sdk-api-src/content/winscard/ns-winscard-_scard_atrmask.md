---
UID: NS:winscard._SCARD_ATRMASK
title: "_SCARD_ATRMASK"
author: windows-sdk-content
description: Used by the SCardLocateCardsByATR function to locate cards.
old-location: security\scard_atrmask.htm
old-project: secauthn
ms.assetid: d7f1a747-a858-4bf6-874a-d76aa4227cd2
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: "*LPSCARD_ATRMASK, *PSCARD_ATRMASK, LPSCARD_ATRMASK, LPSCARD_ATRMASK structure pointer [Security], PSCARD_ATRMASK, PSCARD_ATRMASK structure pointer [Security], SCARD_ATRMASK, SCARD_ATRMASK structure [Security], _SCARD_ATRMASK, _smart_scard_atrmask, security.scard_atrmask, winscard/LPSCARD_ATRMASK, winscard/PSCARD_ATRMASK, winscard/SCARD_ATRMASK"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winscard.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: SCARD_ATRMASK, *PSCARD_ATRMASK, *LPSCARD_ATRMASK
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winscard.h
api_name:
 - SCARD_ATRMASK
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SCARD_ATRMASK structure


## -description


The <b>SCARD_ATRMASK</b> structure is used by 
the <a href="https://msdn.microsoft.com/6c4a644c-033f-4654-b96d-0379e9ac0bb4">SCardLocateCardsByATR</a> function to locate cards.


## -struct-fields




### -field cbAtr

The number of bytes in the ATR and the mask.


### -field rgbAtr

An array of <b>BYTE</b> values for the ATR of the card with extra alignment bytes.


### -field rgbMask

An array of <b>BYTE</b> values for the mask for the ATR with extra alignment bytes.

