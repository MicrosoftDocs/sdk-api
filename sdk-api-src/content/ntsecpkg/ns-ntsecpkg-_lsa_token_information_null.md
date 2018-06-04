---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _LSA_TOKEN_INFORMATION_NULL structure


## -description


The <b>LSA_TOKEN_INFORMATION_NULL</b> structure is used in cases where a non-authenticated system access is needed.

For example, a non-authentication network circuit (such as a null session) can be given <b>NULL</b> information. This results in an anonymous token being generated for the logon. An anonymous token gives the user no ability to access protected system resources, but does allow access to non-protected system resources.


## -struct-fields




### -field ExpirationTime

Time at which the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> becomes not valid. Use a value in the distant future if the context never expires.


### -field Groups


<a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure containing the <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) of groups the user is to be made a member of. This should not include WORLD or other SIDs defined and assigned by the system. 




Each SID is expected to be in a separately allocated block of memory. The <a href="https://msdn.microsoft.com/library/windows/hardware/ff556834">TOKEN_GROUPS</a> structure is also expected to be in a separately allocated block of memory.

