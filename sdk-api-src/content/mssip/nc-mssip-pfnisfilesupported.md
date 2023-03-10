---
UID: NC:mssip.pfnIsFileSupported
title: pfnIsFileSupported (mssip.h)
description: Queries the subject interface packages (SIPs) listed in the registry to determine which SIP handles the file type. (pfnIsFileSupported)
helpviewer_keywords: ["mssip/pfnIsFileSupported","pfnIsFileSupported","pfnIsFileSupported callback","pfnIsFileSupported callback function [Security]","security.pfnisfilesupported"]
old-location: security\pfnisfilesupported.htm
tech.root: security
ms.assetid: cf12d057-328a-4975-b7e5-842c4ea2e760
ms.date: 12/05/2018
ms.keywords: mssip/pfnIsFileSupported, pfnIsFileSupported, pfnIsFileSupported callback, pfnIsFileSupported callback function [Security], security.pfnisfilesupported
req.header: mssip.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - pfnIsFileSupported
 - mssip/pfnIsFileSupported
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mssip.h
api_name:
 - pfnIsFileSupported
---

# pfnIsFileSupported callback function


## -description

The <b>pfnIsFileSupported</b> callback function queries the <a href="/windows/desktop/SecGloss/s-gly">subject interface packages</a> (SIPs) listed in the registry to determine which SIP handles the file type.

## -parameters

### -param hFile [in]

A handle to the file.

### -param pgSubject [out]

The GUID that identifies the SIP that handles the file type.

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

If the SIP supports the file type passed by <i>hfile</i>, the function returns <b>TRUE</b>, and sets <i>pgSubject</i> to the GUID that identifies the SIP for handling the file type.

Each SIP implements its own version of the function that determines whether the file type is supported. The specific name of the function may vary depending on the implementation of the SIP, but the signature of the function will match that of the [SIP_ADD_NEWPROVIDER](/windows/desktop/api/mssip/ns-mssip-sip_add_newprovider) structure.
