---
UID: NS:winnt._TOKEN_ORIGIN
title: "_TOKEN_ORIGIN"
author: windows-sdk-content
description: Contains information about the origin of the logon session.
old-location: security\token_origin.htm
tech.root: SecAuthZ
ms.assetid: b613f76a-7ad1-4066-90a1-244974f10219
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PTOKEN_ORIGIN, PTOKEN_ORIGIN, PTOKEN_ORIGIN structure pointer [Security], TOKEN_ORIGIN, TOKEN_ORIGIN structure [Security], _TOKEN_ORIGIN, security.token_origin, winnt/PTOKEN_ORIGIN, winnt/TOKEN_ORIGIN"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
 - HeaderDef
api_location:
 - Winnt.h
api_name:
 - TOKEN_ORIGIN
product: Windows
targetos: Windows
req.typenames: TOKEN_ORIGIN, *PTOKEN_ORIGIN
req.redist: 
---

# _TOKEN_ORIGIN structure


## -description


The <b>TOKEN_ORIGIN</b> structure contains information about  the origin of the logon session. This structure is used by the <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function.


## -struct-fields




### -field OriginatingLogonSession

<a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Locally unique identifier</a> (LUID) for the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>. If the token  passed to <a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> resulted from a logon using explicit credentials, such as passing name, domain, and password to the  <a href="https://msdn.microsoft.com/a6d880a0-0aed-4bdb-89c9-4f667ecb510e">LogonUser</a> function, then this member will contain the ID of the <i>logon session</i> that created it.  If the token resulted from  network authentication, such as a call to <a href="security.acceptsecuritycontext">AcceptSecurityContext</a>,  or a call to <b>LogonUser</b> with <i>dwLogonType</i> set to LOGON32_LOGON_NETWORK or LOGON32_LOGON_NETWORK_CLEARTEXT, then this member will be zero.


## -see-also




<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>
 

 

