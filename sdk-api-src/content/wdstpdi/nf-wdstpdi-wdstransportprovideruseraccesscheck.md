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

# WdsTransportProviderUserAccessCheck function


## -description


Specifies access to a content stream based on a user's token. 


## -parameters




### -param hContent [in]

Handle to an open content stream to be read. This is the handle return by the <a href="https://msdn.microsoft.com/95bea971-9c97-4d66-871d-5ef7407b9659">WdsTransportProviderOpenContent</a> callback.


### -param hUserToken [in]

The token of the user whose access should be checked.


### -param pbAccessAllowed [out]

Pointer to a boolean value. The content provider should set this value to <b>TRUE</b> if it allows the user access to the content stream.  The content provider should set this value to <b>FALSE</b> if it does not allow the user access to the content stream.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This callback is required.



