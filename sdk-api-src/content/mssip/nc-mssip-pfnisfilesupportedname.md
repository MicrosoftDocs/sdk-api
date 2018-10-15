---
UID: NC:mssip.pfnIsFileSupportedName
title: pfnIsFileSupportedName
author: windows-sdk-content
description: Queries the subject interface packages (SIPs) listed in the registry to determine which SIP handles the file type.
old-location: security\pfnisfilesupportedname.htm
tech.root: seccrypto
ms.assetid: cc2304ef-c319-45eb-b2ec-7410510af213
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: mssip/pfnIsFileSupportedName, pfnIsFileSupportedName, pfnIsFileSupportedName callback, pfnIsFileSupportedName callback function [Security], security.pfnisfilesupportedname
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
 - pfnIsFileSupportedName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# pfnIsFileSupportedName callback function


## -description


The <b>pfnIsFileSupportedName</b> callback function queries the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface packages</a> (SIPs) listed in the registry to determine which SIP handles the file type.


## -parameters




### -param *pwszFileName [in]

A pointer to a <b>null</b>-terminated string that contains the absolute path to the file to be processed by the SIP.


### -param *pgSubject [out]

The GUID identifying the SIP that handles the file type.


## -returns



The return value is <b>TRUE</b> if the function succeeds; <b>FALSE</b> if the function fails. If the function fails, call the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function to determine the reason for failure.




## -remarks



If the SIP supports the file type passed by <i>hfile</i>, the function returns <b>TRUE</b>, and sets <i>pgSubject</i> to the GUID that identifies the SIP for handling the file type.

Each SIP implements its own version of the function that determines if the file type is supported. The specific name of the function may vary depending on the implementation of the SIP, but the signature of the function will match that of the <b>pfnIsFileSupportedName</b> function.  The function name is added to the registry by the <a href="https://msdn.microsoft.com/99633c2f-e5ed-49e4-9c98-7501f66e5571">CryptSIPAddProvider</a> function, which takes the function name as parameter in the <b>pwszIsFunctionNameFmt2</b> field in the <a href="https://msdn.microsoft.com/5ca88c0c-a7c9-4517-a874-49d38c1bc7c3">SIP_ADD_NEWPROVIDER</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/cf12d057-328a-4975-b7e5-842c4ea2e760">pfnIsFileSupported</a>
 

 

