---
UID: NS:winnt._TOKEN_CONTROL
title: "_TOKEN_CONTROL"
author: windows-sdk-content
description: Contains information that identifies an access token.
old-location: security\token_control.htm
old-project: secauthz
ms.assetid: b87c942b-8e58-471d-8cdf-e46cdac647c4
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: "*PTOKEN_CONTROL, PTOKEN_CONTROL, PTOKEN_CONTROL structure pointer [Security], TOKEN_CONTROL, TOKEN_CONTROL structure [Security], _TOKEN_CONTROL, _win32_token_control_str, security.token_control, winnt/PTOKEN_CONTROL, winnt/TOKEN_CONTROL"
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
req.typenames: TOKEN_CONTROL, *PTOKEN_CONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_CONTROL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _TOKEN_CONTROL structure


## -description


The <b>TOKEN_CONTROL</b> structure contains information that identifies an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>.


## -struct-fields




### -field TokenId

Specifies a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">locally unique identifier</a> (LUID) identifying this instance of the token object.


### -field AuthenticationId

Specifies an LUID assigned to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session</a> this token represents. There can be many tokens representing a single <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.


### -field ModifiedId

Specifies an LUID that changes each time the token is modified. An application can use this value as a test of whether a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> has changed since it was last used.


### -field TokenSource

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a> structure identifying the agency that issued the token. This information is used in audit trails.


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556831">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556838">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556842">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556845">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556849">TOKEN_STATISTICS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556851">TOKEN_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556855">TOKEN_USER</a>
 

 

