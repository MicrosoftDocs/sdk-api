---
UID: NF:mscat.CryptCATHandleFromStore
title: CryptCATHandleFromStore function (mscat.h)
description: Retrieves a catalog handle from memory.
helpviewer_keywords: ["CryptCATHandleFromStore","CryptCATHandleFromStore function [Security]","mscat/CryptCATHandleFromStore","security.cryptcathandlefromstore"]
old-location: security\cryptcathandlefromstore.htm
tech.root: security
ms.assetid: e9aedc2d-9492-4ed7-9f2d-891997f85f6f
ms.date: 12/05/2018
ms.keywords: CryptCATHandleFromStore, CryptCATHandleFromStore function [Security], mscat/CryptCATHandleFromStore, security.cryptcathandlefromstore
req.header: mscat.h
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATHandleFromStore
 - mscat/CryptCATHandleFromStore
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATHandleFromStore
---

# CryptCATHandleFromStore function


## -description

<p class="CCE_Message">[The  <b>CryptCATHandleFromStore</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATHandleFromStore</b> function retrieves a catalog handle from memory.

## -parameters

### -param pCatStore [in]

A pointer to a [CRYPTCATSTORE](/windows/desktop/api/mscat/ns-mscat-cryptcatstore) structure that contains the handle to retrieve.

## -returns

A handle to the catalog.