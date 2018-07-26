---
UID: NF:securitybaseapi.CheckTokenMembershipEx
title: CheckTokenMembershipEx function
author: windows-sdk-content
description: Determines whether the specified SID is enabled in the specified token.
old-location: security\checktokenmembershipex.htm
old-project: secauthz
ms.assetid: 0420FC77-8035-42A5-8907-83D0CE53FB64
ms.author: windowssdkdev
ms.date: 07/19/2018
ms.keywords: CheckTokenMembershipEx, CheckTokenMembershipEx function [Security], security.checktokenmembershipex, securitybaseapi/CheckTokenMembershipEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: securitybaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - CheckTokenMembershipEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# CheckTokenMembershipEx function


## -description


The <b>CheckTokenMembershipEx</b> function determines whether the specified SID is enabled in the specified token.


## -parameters




### -param TokenHandle [in, optional]

A handle to an access token. If present, this token is checked for the SID. If not present, then the current effective token is used. This must be an impersonation token.


### -param SidToCheck [in]

A pointer to a SID structure. The function checks for the presence of this SID in the presence of the token.


### -param Flags [in]

Flags that affect the behavior of the function. Currently the only valid flag is CTMF_INCLUDE_APPCONTAINER which allows app containers to pass the call as long as the other requirements of the token are met, such as the group specified is present and enabled.


### -param IsMember [out]

<b>TRUE</b> if the SID is enabled in the token; otherwise, <b>FALSE</b>.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



