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

# IConnectedIdentityProvider::GetUrl


## -description


Returns the URL string for the specified wizard or webpage.


## -parameters




### -param Identifier [in]

Identifies the wizard or webpage that should be returned.


### -param Context [in]

Describes the context in which the URL will be displayed.


### -param PostData [out]

A <b>VARIANT</b> of type VT_ARRAY and VT_UI1 that will be posted to the provided URL. If the post data is not required, this parameter should be set to VT_EMPTY.


### -param Url [out]

Returns a URL for the specified identity wizard or webpage. The URL must begin with <b>https://</b>.


## -returns



If the method succeeds, the method returns S_OK.

If the method fails, the method returns a Win32 error code.




## -see-also




<a href="https://msdn.microsoft.com/0AF5036B-326E-4FBE-9F26-18F532EF0BB3">IConnectedIdentityProvider</a>
 

 

