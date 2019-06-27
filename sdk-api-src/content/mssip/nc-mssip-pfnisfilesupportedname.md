---
UID: NC:mssip.pfnIsFileSupportedName
title: pfnIsFileSupportedName (mssip.h)
author: windows-sdk-content
description: Queries the subject interface packages (SIPs) listed in the registry to determine which SIP handles the file type.
old-location: security\pfnisfilesupportedname.htm
tech.root: SecCrypto
ms.assetid: cc2304ef-c319-45eb-b2ec-7410510af213
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: mssip/pfnIsFileSupportedName, pfnIsFileSupportedName, pfnIsFileSupportedName callback, pfnIsFileSupportedName callback function [Security], security.pfnisfilesupportedname
ms.topic: callback
f1_keywords: 
 - "mssip/pfnIsFileSupportedName"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mssip.h
api_name:
 - pfnIsFileSupportedName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# pfnIsFileSupportedName callback function


## -description


The <b>pfnIsFileSupportedName</b> callback function queries the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">subject interface packages</a> (SIPs) listed in the registry to determine which SIP handles the file type.


## -parameters




### -param *pwszFileName [in]

A pointer to a <b>null</b>-terminated string that contains the absolute path to the file to be processed by the SIP.


### -param *pgSubject [out]

The GUID identifying the SIP that handles the file type.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails. If the function fails, call the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function to determine the reason for failure.




## -remarks



If the SIP supports the file type passed by <i>hfile</i>, the function returns <b>TRUE</b>, and sets <i>pgSubject</i> to the GUID that identifies the SIP for handling the file type.

Each SIP implements its own version of the function that determines if the file type is supported. The specific name of the function may vary depending on the implementation of the SIP, but the signature of the function will match that of the <b>pfnIsFileSupportedName</b> function.  The function name is added to the registry by the <a href="https://docs.microsoft.com/windows/desktop/api/mssip/nf-mssip-cryptsipaddprovider">CryptSIPAddProvider</a> function, which takes the function name as parameter in the <b>pwszIsFunctionNameFmt2</b> field in the <a href="https://docs.microsoft.com/windows/desktop/api/mssip/ns-mssip-sip_add_newprovider_">SIP_ADD_NEWPROVIDER</a> structure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mssip/nc-mssip-pfnisfilesupported">pfnIsFileSupported</a>
 

 

