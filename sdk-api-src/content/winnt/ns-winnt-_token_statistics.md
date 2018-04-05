---
UID: NS:winnt._TOKEN_STATISTICS
title: "_TOKEN_STATISTICS"
author: windows-driver-content
description: Contains information about an access token.
old-location: security\token_statistics.htm
old-project: SecAuthZ
ms.assetid: 7fcc4a46-1bac-49c1-a239-b466d3bf31d9
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: "*PTOKEN_STATISTICS, PTOKEN_STATISTICS, PTOKEN_STATISTICS structure pointer [Security], TOKEN_STATISTICS, TOKEN_STATISTICS structure [Security], _TOKEN_STATISTICS, _win32_token_statistics_str, security.token_statistics, winnt/PTOKEN_STATISTICS, winnt/TOKEN_STATISTICS"
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TOKEN_STATISTICS, *PTOKEN_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winnt.h
api_name:
-	TOKEN_STATISTICS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _TOKEN_STATISTICS structure


## -description


The <b>TOKEN_STATISTICS</b> structure contains information about an <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a>. An application can retrieve this information by calling the 
<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a> function.


## -struct-fields




### -field TokenId

Specifies a locally unique identifier (<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>) that identifies this instance of the token object.


### -field AuthenticationId

Specifies an LUID assigned to the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">session</a> this token represents. There can be many tokens representing a single <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">logon session</a>.


### -field ExpirationTime

Specifies the time at which this token expires. Expiration times for access tokens are not currently supported.


### -field TokenType

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556851">TOKEN_TYPE</a> enumeration type indicating whether the token is a <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary</a> or <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>.


### -field ImpersonationLevel

Specifies a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a> enumeration type indicating the impersonation level of the token. This member is valid only if the <b>TokenType</b> is TokenImpersonation.


### -field DynamicCharged

Specifies the amount, in bytes, of memory allocated for storing default protection and a primary group identifier.


### -field DynamicAvailable

Specifies the portion of memory allocated for storing default protection and a primary group identifier not already in use. This value is returned as a count of free bytes.


### -field GroupCount

Specifies the number of supplemental group <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) included in the token.


### -field PrivilegeCount

Specifies the number of privileges included in the token.


### -field ModifiedId

Specifies an LUID that changes each time the token is modified. An application can use this value as a test of whether a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> has changed since it was last used.


## -see-also




<a href="https://msdn.microsoft.com/e94de19c-de12-40fb-a72c-060f7ad12f75">GetTokenInformation</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556827">TOKEN_CONTROL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556831">TOKEN_DEFAULT_DACL</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556838">TOKEN_INFORMATION_CLASS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556842">TOKEN_OWNER</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556845">TOKEN_PRIMARY_GROUP</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556846">TOKEN_PRIVILEGES</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556848">TOKEN_SOURCE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556851">TOKEN_TYPE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556855">TOKEN_USER</a>
 

 

