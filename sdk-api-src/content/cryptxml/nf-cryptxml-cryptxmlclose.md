---
UID: NF:cryptxml.CryptXmlClose
title: CryptXmlClose function (cryptxml.h)
description: Closes a cryptographic XML object handle.
helpviewer_keywords: ["CryptXmlClose","CryptXmlClose function [Security]","cryptxml/CryptXmlClose","security.cryptxmlclose"]
old-location: security\cryptxmlclose.htm
tech.root: security
ms.assetid: ee3f8ea3-4898-462b-87cd-47dd3134636c
ms.date: 12/05/2018
ms.keywords: CryptXmlClose, CryptXmlClose function [Security], cryptxml/CryptXmlClose, security.cryptxmlclose
req.header: cryptxml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptxml.lib
req.dll: Cryptxml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptXmlClose
 - cryptxml/CryptXmlClose
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptxml.dll
api_name:
 - CryptXmlClose
---

# CryptXmlClose function


## -description

The <b>CryptXmlClose</b> function closes a cryptographic XML object handle.

## -parameters

### -param hCryptXml [in]

The handle of the cryptographic XML object to be closed.

## -returns

If the function succeeds, the function returns zero.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error.

## -remarks

At each call to this function, the reference count on the handle is reduced by one. When the reference count reaches zero, an object encapsulated by the handle is fully released.

