---
UID: NF:bcrypt.BCryptFreeBuffer
title: BCryptFreeBuffer function (bcrypt.h)
description: Used to free memory that was allocated by one of the CNG functions.
helpviewer_keywords: ["BCryptFreeBuffer","BCryptFreeBuffer function [Security]","bcrypt/BCryptFreeBuffer","security.bcryptfreebuffer_func"]
old-location: security\bcryptfreebuffer_func.htm
tech.root: security
ms.assetid: 0ee83ca1-2fe6-4ff2-823e-888b3e66f310
ms.date: 12/05/2018
ms.keywords: BCryptFreeBuffer, BCryptFreeBuffer function [Security], bcrypt/BCryptFreeBuffer, security.bcryptfreebuffer_func
req.header: bcrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bcrypt.lib
req.dll: Bcrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - BCryptFreeBuffer
 - bcrypt/BCryptFreeBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Bcrypt.dll
 - Ksecdd.sys
api_name:
 - BCryptFreeBuffer
---

# BCryptFreeBuffer function


## -description

The <b>BCryptFreeBuffer</b> function is used to free memory that was allocated by one of the CNG functions.

## -parameters

### -param pvBuffer [in]

A pointer to the memory buffer to be freed.

## -remarks

<b>BCryptFreeBuffer</b> must be called in the same processor mode as the BCrypt API function that allocated the buffer. In addition, if the buffer was allocated at <b>PASSIVE_LEVEL</b> <a href="/windows/desktop/SecGloss/i-gly">IRQL</a>, it must be freed at that <i>IRQL</i>. If the buffer was allocated at <b>DISPATCH_LEVEL</b> <i>IRQL</i>, it can be freed at either <b>DISPATCH_LEVEL</b> <i>IRQL</i> or <b>PASSIVE_LEVEL</b> <i>IRQL</i>.

To call this function in kernel mode, use Cng.lib, which is part of the Driver Development Kit (DDK). <b>Windows Server 2008 and Windows Vista:  </b>To call this function in kernel mode, use Ksecdd.lib.

## -see-also

<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumcontexts">BCryptEnumContexts</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptenumregisteredproviders">BCryptEnumRegisteredProviders</a>



<a href="/windows/desktop/api/bcrypt/nf-bcrypt-bcryptqueryproviderregistration">BCryptQueryProviderRegistration</a>