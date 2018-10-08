---
UID: NF:ntsecapi.LsaEnumerateLogonSessions
title: LsaEnumerateLogonSessions function
author: windows-sdk-content
description: Retrieves the set of existing logon session identifiers (LUIDs) and the number of sessions.
old-location: security\lsaenumeratelogonsessions.htm
tech.root: secauthn
ms.assetid: ddf3b9ec-dea7-4333-9ffe-142811048c83
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: LsaEnumerateLogonSessions, LsaEnumerateLogonSessions function [Security], _lsa_lsaenumeratelogonsessions, ntsecapi/LsaEnumerateLogonSessions, security.lsaenumeratelogonsessions
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecapi.h
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - LsaEnumerateLogonSessions
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsaEnumerateLogonSessions function


## -description


The <b>LsaEnumerateLogonSessions</b> function retrieves the set of existing logon session identifiers (<a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUIDs</a>) and the number of sessions.


## -parameters




### -param LogonSessionCount [out]

Pointer to a long integer that receives the number of elements returned in the array returned in <i>LogonSessionList</i> parameter.


### -param LogonSessionList [out]

Address of a pointer to a LUID. The pointer receives the first element of an array of logon session identifiers. The memory used by the array is allocated by the LSA. When the array is no longer needed, call the 
<a href="https://msdn.microsoft.com/e814ed68-07e7-4936-ba96-5411086f43f6">LSAFreeReturnBuffer</a> function to free it.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason.




## -remarks



To retrieve information about the logon sessions returned by <b>LsaEnumerateLogonSessions</b>, call the 
<a href="https://msdn.microsoft.com/b1478a7a-f508-4b98-8c7b-adeb2f07bb86">LsaGetLogonSessionData</a> function.



