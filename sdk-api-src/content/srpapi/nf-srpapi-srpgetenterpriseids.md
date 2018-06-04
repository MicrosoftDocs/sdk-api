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

# SrpGetEnterpriseIds function


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy cannot be applied on Windows 10, version 1511 (build 10586) or earlier.</div>
<div> </div>Gets the list of enterprise identifiers for the given token.

The enterprise IDs are returned only for those applications explicitly allowed by management.


## -parameters




### -param tokenHandle [in]

Token Handle to be checked.


### -param numberOfBytes [in, out, optional]

If <i>enterpriseIds</i> is provided, then this supplies the size of the <i>enterpriseIds</i> buffer. If you provide a buffer size, and it's too small, the output will contain the required size of the <i>enterpriseIds</i> buffer. 


### -param enterpriseIds [out, optional]

An array of enterprise ID string pointers.


### -param enterpriseIdCount [out]

The enterprise ID count on the token. Zero if the token is not explicitly enterprise allowed.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

If this function does not provide any enterprise IDs, it returns <b>E_NOT_SUFFICIENT_BUFFER</b>.



