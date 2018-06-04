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

# IWorkspace3::GetClaimsToken2


## -description


Retrieves a claims token.


## -parameters




### -param bstrClaimsHint [in]

String containing the claims hint.


### -param bstrUserHint [in]

String containing the user hint.


### -param claimCookie [in]

The claim cookie.


### -param hwndCredUiParent [in]

Handle of the parent UI element the request came from.


### -param rectCredUiParent [in]

Pointer to a RECT structure that contains the X and Y coordinates of the parent UI.


### -param pbstrAccessToken [out, retval]

On success, return a pointer to a string containing the access token.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/a63240fb-8724-4cd2-b845-f48075f4cb57">IWorkspace3</a>
 

 

