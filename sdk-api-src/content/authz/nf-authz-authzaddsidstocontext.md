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

# AuthzAddSidsToContext function


## -description


The <b>AuthzAddSidsToContext</b> function creates a copy of an existing context and appends a given set of <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifiers</a> (SIDs) and restricted SIDs.


## -parameters




### -param hAuthzClientContext

TBD


### -param Sids [in]

A pointer to a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556742">SID_AND_ATTRIBUTES</a> structure containing the SIDs and attributes to be added to the unrestricted part of the client context.


### -param SidCount [in]

The number of SIDs to be added.


### -param RestrictedSids [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff556742">SID_AND_ATTRIBUTES</a> structure containing the SIDs and attributes to be added to the restricted part of the client context.


### -param RestrictedSidCount [in]

Number of restricted SIDs to be added.


### -param phNewAuthzClientContext

TBD




#### - OrigClientContext [in]

An <b>AUTHZ_CLIENT_CONTEXT_HANDLE</b> structure to be copied as the basis for <i>NewClientContext</i>.


#### - pNewClientContext [out]

A pointer to the created <b>AUTHZ_CLIENT_CONTEXT_HANDLE</b> structure containing input values for expiration time, identifier, flags, additional SIDs and restricted SIDs.


## -returns



If the function succeeds, it returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="authorization_functions.htm">Basic Access Control Functions</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556742">SID_AND_ATTRIBUTES</a>
 

 

