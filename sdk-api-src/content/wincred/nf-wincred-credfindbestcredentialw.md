---
UID: NF:wincred.CredFindBestCredentialW
title: CredFindBestCredentialW function
author: windows-sdk-content
description: Searches the Credentials Management (CredMan) database for the set of generic credentials that are associated with the current logon session and that best match the specified target resource.
old-location: security\credfindbestcredential.htm
tech.root: secauthn
ms.assetid: b39e3167-dd63-4b81-b850-f3117be348a5
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: CredFindBestCredential, CredFindBestCredential function [Security], CredFindBestCredentialA, CredFindBestCredentialW, security.credfindbestcredential, wincred/CredFindBestCredential, wincred/CredFindBestCredentialA, wincred/CredFindBestCredentialW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincred.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CredFindBestCredentialW (Unicode) and CredFindBestCredentialA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - sechost.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredFindBestCredential
 - CredFindBestCredentialA
 - CredFindBestCredentialW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CredFindBestCredentialW function


## -description


The <b>CredFindBestCredential</b> function searches the <a href="https://msdn.microsoft.com/0c44a360-d9c3-448c-a0d5-e33f3c27c58c">Credentials Management</a> (CredMan) database for the set of generic credentials that are associated with the current logon session and that best match the specified target resource.


## -parameters




### -param TargetName [in]

A pointer to a null-terminated string that contains the name of the target resource for which to find credentials.


### -param Type [in]

The type of credentials to search for. Currently, this function supports only <b>CRED_TYPE_GENERIC</b>.


### -param Flags [in]

Reserved.


### -param Credential [out]

The address of a pointer to a <a href="https://msdn.microsoft.com/6361b93c-4441-4a01-bd39-b95c42962497">CREDENTIAL</a> structure that specifies the set of credentials this function finds.

When you have finished using this structure, free it by calling the <a href="https://msdn.microsoft.com/bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada">CredFree</a> function.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.



