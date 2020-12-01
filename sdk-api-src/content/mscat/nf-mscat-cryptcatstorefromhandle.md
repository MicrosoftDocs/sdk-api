---
UID: NF:mscat.CryptCATStoreFromHandle
title: CryptCATStoreFromHandle function (mscat.h)
description: Retrieves a CRYPTCATSTORE structure from a catalog handle.
helpviewer_keywords: ["CryptCATStoreFromHandle","CryptCATStoreFromHandle function [Security]","mscat/CryptCATStoreFromHandle","security.cryptcatstorefromhandle"]
old-location: security\cryptcatstorefromhandle.htm
tech.root: security
ms.assetid: ce4fe972-0ed5-4b18-8ec5-9883af326335
ms.date: 12/05/2018
ms.keywords: CryptCATStoreFromHandle, CryptCATStoreFromHandle function [Security], mscat/CryptCATStoreFromHandle, security.cryptcatstorefromhandle
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
 - CryptCATStoreFromHandle
 - mscat/CryptCATStoreFromHandle
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
 - CryptCATStoreFromHandle
---

# CryptCATStoreFromHandle function


## -description

<p class="CCE_Message">[The  <b>CryptCATStoreFromHandle</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The [CRYPTCATSTORE](/windows/desktop/api/mscat/ns-mscat-cryptcatstore) structure from a catalog handle.

## -parameters

### -param hCatalog [in]

A handle to the catalog obtained from the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> or <a href="/windows/desktop/api/mscat/nf-mscat-cryptcathandlefromstore">CryptCATHandleFromStore</a> function.

## -returns

A pointer to a [CRYPTCATSTORE](/windows/desktop/api/mscat/ns-mscat-cryptcatstore) structure that contains the catalog store. The caller must not free this pointer or any of its members.