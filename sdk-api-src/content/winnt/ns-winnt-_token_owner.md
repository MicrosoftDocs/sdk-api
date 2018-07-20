---
UID: NS:winnt._TOKEN_OWNER
title: "_TOKEN_OWNER"
author: windows-sdk-content
description: Contains the default owner security identifier (SID) that will be applied to newly created objects.
old-location: security\token_owner.htm
old-project: SecAuthZ
ms.assetid: 85617d56-ad46-40a3-a335-121f3c8edcc3
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: "*PTOKEN_OWNER, PTOKEN_OWNER, PTOKEN_OWNER structure pointer [Security], TOKEN_OWNER, TOKEN_OWNER structure [Security], _TOKEN_OWNER, _win32_token_owner_str, security.token_owner, winnt/PTOKEN_OWNER, winnt/TOKEN_OWNER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
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
tech.root: 
req.typenames: TOKEN_OWNER, *PTOKEN_OWNER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_OWNER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _TOKEN_OWNER structure


## -description



			The <b>TOKEN_OWNER</b> structure contains the default owner <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) that will be applied to newly created objects.


## -struct-fields




### -field Owner

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure representing a user who will become the owner of any objects created by a process using this <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>. The SID must be one of the user or group SIDs already in the token.


## -see-also




<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a>



<a href="https://msdn.microsoft.com/cdb8af74-540d-4059-ac64-6243f6aabaa6">SetTokenInformation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556827">TOKEN_CONTROL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556831">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556838">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556845">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556849">TOKEN_STATISTICS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556851">TOKEN_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556855">TOKEN_USER</a>
 

 

