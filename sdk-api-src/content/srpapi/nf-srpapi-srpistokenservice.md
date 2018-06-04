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

# SrpIsTokenService function


## -description



<div class="alert"><b>Note</b>  Windows Information Protection (WIP) policy cannot be applied on Windows 10, version 1511 (build 10586) or earlier.</div>
<div> </div>Identifies whether a service is a token service. 


## -parameters




### -param TokenHandle

TBD


### -param IsTokenService [out]

A boolean value that indicates whether the service is a token service.


#### - tokenHandle [in]

Token Handle to be checked.


## -returns



If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.



