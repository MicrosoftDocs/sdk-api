---
UID: NC:mssip.pfnIsFileSupported
title: pfnIsFileSupported
author: windows-sdk-content
description: Queries the subject interface packages (SIPs) listed in the registry to determine which SIP handles the file type.
old-location: security\pfnisfilesupported.htm
tech.root: seccrypto
ms.assetid: cf12d057-328a-4975-b7e5-842c4ea2e760
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: mssip/pfnIsFileSupported, pfnIsFileSupported, pfnIsFileSupported callback, pfnIsFileSupported callback function [Security], security.pfnisfilesupported
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
 - pfnIsFileSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# pfnIsFileSupported callback function


## -description


The <b>pfnIsFileSupported</b> callback function queries the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface packages</a> (SIPs) listed in the registry to determine which SIP handles the file type.


## -parameters




### -param hFile [in]

A handle to the file.


### -param *pgSubject [out]

The GUID that identifies the SIP that handles the file type.


## -returns



If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



If the SIP supports the file type passed by <i>hfile</i>, the function returns <b>TRUE</b>, and sets <i>pgSubject</i> to the GUID that identifies the SIP for handling the file type.

Each SIP implements its own version of the function that determines whether the file type is supported. The specific name of the function may vary depending on the implementation of the SIP, but the signature of the function will match that of the <b>pfnIsFileSupported</b> function.  The function name is added to the registry by the <a href="https://msdn.microsoft.com/99633c2f-e5ed-49e4-9c98-7501f66e5571">CryptSIPAddProvider</a> function, which takes the function name as a parameter in the <b>pwszIsFunctionName</b> field of the <a href="https://msdn.microsoft.com/5ca88c0c-a7c9-4517-a874-49d38c1bc7c3">SIP_ADD_NEWPROVIDER</a> structure.



