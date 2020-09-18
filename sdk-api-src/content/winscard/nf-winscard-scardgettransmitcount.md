---
UID: NF:winscard.SCardGetTransmitCount
title: SCardGetTransmitCount function (winscard.h)
description: Retrieves the number of transmit operations that have completed since the specified card reader was inserted.
helpviewer_keywords: ["SCardGetTransmitCount","SCardGetTransmitCount function [Security]","security.scardgettransmitcount","winscard/SCardGetTransmitCount"]
old-location: security\scardgettransmitcount.htm
tech.root: security
ms.assetid: 13857fc3-374d-4ba5-b4ca-e523b323974c
ms.date: 12/05/2018
ms.keywords: SCardGetTransmitCount, SCardGetTransmitCount function [Security], security.scardgettransmitcount, winscard/SCardGetTransmitCount
req.header: winscard.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Winscard.lib
req.dll: Winscard.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SCardGetTransmitCount
 - winscard/SCardGetTransmitCount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Winscard.dll
api_name:
 - SCardGetTransmitCount
---

# SCardGetTransmitCount function


## -description

The <b>SCardGetTransmitCount</b> function retrieves the number of transmit operations that have completed since the specified card reader was inserted.

## -parameters

### -param hCard [in]

A handle to a smart card obtained from a previous call to 
<a href="/windows/desktop/api/winscard/nf-winscard-scardconnecta">SCardConnect</a>.

### -param pcTransmitCount [out]

A pointer to the number of transmit operations that have completed since the specified card reader was inserted.

## -returns

If the function succeeds, it returns <b>SCARD_S_SUCCESS</b>. 

If the function fails, it returns an error code. For more information, see <a href="/windows/desktop/SecAuthN/authentication-return-values">Smart Card Return Values</a>.