---
UID: NS:ntsecpkg._LSA_TOKEN_INFORMATION_NULL
title: "_LSA_TOKEN_INFORMATION_NULL"
author: windows-sdk-content
description: Used in cases where a non-authenticated system access is needed.
old-location: security\lsa_token_information_null.htm
old-project: SecAuthN
ms.assetid: fbcd0f78-1ad5-4bea-a95f-d19fb3894537
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PLSA_TOKEN_INFORMATION_NULL, LSA_TOKEN_INFORMATION_NULL, LSA_TOKEN_INFORMATION_NULL structure [Security], PLSA_TOKEN_INFORMATION_NULL, PLSA_TOKEN_INFORMATION_NULL structure pointer [Security], _LSA_TOKEN_INFORMATION_NULL, _lsa_lsa_token_information_null, ntsecpkg/LSA_TOKEN_INFORMATION_NULL, ntsecpkg/PLSA_TOKEN_INFORMATION_NULL, security.lsa_token_information_null"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ntsecpkg.h
req.include-header: 
req.redist: 
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
req.typenames: LSA_TOKEN_INFORMATION_NULL, *PLSA_TOKEN_INFORMATION_NULL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntsecpkg.h
api_name:
 - LSA_TOKEN_INFORMATION_NULL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _LSA_TOKEN_INFORMATION_NULL structure


## -description


The <b>LSA_TOKEN_INFORMATION_NULL</b> structure is used in cases where a non-authenticated system access is needed.

For example, a non-authentication network circuit (such as a null session) can be given <b>NULL</b> information. This results in an anonymous token being generated for the logon. An anonymous token gives the user no ability to access protected system resources, but does allow access to non-protected system resources.


## -struct-fields




### -field ExpirationTime

Time at which the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> becomes not valid. Use a value in the distant future if the context never expires.


### -field Groups


<a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure containing the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) of groups the user is to be made a member of. This should not include WORLD or other SIDs defined and assigned by the system. 




Each SID is expected to be in a separately allocated block of memory. The <a href="https://msdn.microsoft.com/387dd7f8-4177-40fa-b5fd-bb4b371a0e64">TOKEN_GROUPS</a> structure is also expected to be in a separately allocated block of memory.

