---
UID: NF:wincred.CredFree
title: CredFree function
author: windows-sdk-content
description: The CredFree function frees a buffer returned by any of the credentials management functions.
old-location: security\credfree.htm
tech.root: secauthn
ms.assetid: bc33ab1b-dd3f-4e1b-96d2-e32ceff89ada
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CredFree, CredFree function [Security], _cred_credfree, security.credfree, wincred/CredFree
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincred.h
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
 - API-MS-Win-DownLevel-AdvApi32-l2-1-0.dll
 - sechost.dll
 - API-MS-Win-DownLevel-AdvApi32-l2-1-1.dll
 - API-MS-Win-Security-credentials-l1-1-0.dll
api_name:
 - CredFree
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CredFree function


## -description


The <b>CredFree</b> function frees a buffer returned by any of the credentials management functions.


## -parameters




### -param Buffer [in]

Pointer to the buffer to be freed.


## -returns



This function does not return a value.



