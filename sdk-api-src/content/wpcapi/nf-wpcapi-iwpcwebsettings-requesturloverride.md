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

# IWPCWebSettings::RequestURLOverride


## -description


Requests that the Parental Controls web restrictions subsystem set the specified primary and sub URLs to the allowed state.


## -parameters




### -param hWnd [in]

A handle to the parent window. This is  needed for proper User Account Control (UAC) dialog box behavior.


### -param pcszURL [in]

A pointer to primary URL for override.


### -param cURLs [in]

The number of entries in <i>ppcszSubURLs</i>.


### -param ppcszSubURLs [in]

Pointers to URLs that include pages with the primary URL.


### -param pfChanged [out]

Pointer to flag notifying completion of override changed status. This parameter is 1 if the status is changed, and 0 otherwise.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/80629db8-0040-4545-a313-5cf7aa3d7f8b">IWPCWebSettings</a>
 

 

