---
UID: NF:wincred.CredFree
title: CredFree function (wincred.h)
description: The CredFree function frees a buffer returned by any of the credentials management functions.
helpviewer_keywords: ["CredFree","CredFree function [Security]","_cred_credfree","security.credfree","wincred/CredFree"]
old-location: security\credfree.htm
tech.root: security
ms.assetid: bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada
ms.date: 12/05/2018
ms.keywords: CredFree, CredFree function [Security], _cred_credfree, security.credfree, wincred/CredFree
req.header: wincred.h
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CredFree
 - wincred/CredFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredFree
---

# CredFree function


## -description

The <b>CredFree</b> function frees a buffer returned by any of the credentials management functions.

## -parameters

### -param Buffer [in]

Pointer to the buffer to be freed.

