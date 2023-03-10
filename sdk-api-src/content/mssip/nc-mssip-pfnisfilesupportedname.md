---
UID: NC:mssip.pfnIsFileSupportedName
title: pfnIsFileSupportedName (mssip.h)
description: Queries the subject interface packages (SIPs) listed in the registry to determine which SIP handles the file type. (pfnIsFileSupportedName)
helpviewer_keywords: ["mssip/pfnIsFileSupportedName","pfnIsFileSupportedName","pfnIsFileSupportedName callback","pfnIsFileSupportedName callback function [Security]","security.pfnisfilesupportedname"]
old-location: security\pfnisfilesupportedname.htm
tech.root: security
ms.assetid: cc2304ef-c319-45eb-b2ec-7410510af213
ms.date: 12/05/2018
ms.keywords: mssip/pfnIsFileSupportedName, pfnIsFileSupportedName, pfnIsFileSupportedName callback, pfnIsFileSupportedName callback function [Security], security.pfnisfilesupportedname
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
 - pfnIsFileSupportedName
 - mssip/pfnIsFileSupportedName
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
 - pfnIsFileSupportedName
---

# pfnIsFileSupportedName callback function


## -description

The <b>pfnIsFileSupportedName</b> callback function queries the <a href="/windows/desktop/SecGloss/s-gly">subject interface packages</a> (SIPs) listed in the registry to determine which SIP handles the file type.

## -parameters

### -param pwszFileName [in]

A pointer to a <b>null</b>-terminated string that contains the absolute path to the file to be processed by the SIP.

### -param pgSubject [out]

The GUID identifying the SIP that handles the file type.

## -returns

The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails. If the function fails, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to determine the reason for failure.

## -remarks

If the SIP supports the file type passed by <i>hfile</i>, the function returns <b>TRUE</b>, and sets <i>pgSubject</i> to the GUID that identifies the SIP for handling the file type.

Each SIP implements its own version of the function that determines if the file type is supported. The specific name of the function may vary depending on the implementation of the SIP, but the signature of the function will match that of the [SIP_ADD_NEWPROVIDER](/windows/desktop/api/mssip/ns-mssip-sip_add_newprovider) structure.

SIPs must support a limited set of file types and file extensions. The fileSupportedName function must check that the provided file matches one of the file extensions supported by the SIP.  For instance, the WSH SIP supports only the following list of file extensions and checks that the file under validation is a member of the following list: .js, .jse, .vbe, .vbs, or .wsf.

## -see-also

<a href="/windows/desktop/api/mssip/nc-mssip-pfnisfilesupported">pfnIsFileSupported</a>
