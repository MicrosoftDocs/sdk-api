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

# IActionProgress::QueryCancel


## -description


Provides information about whether the action is being canceled.


## -parameters




### -param pfCancelled [out]

Type: <b>BOOL*</b>

A reference to a <b>BOOL</b> value that specifies whether the action is being canceled.


## -returns



Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.




## -remarks



Call this method when a process must know whether an action has been canceled. Implementing this method requires the implementing class to query either an internal or external flag to provide this information, and store the result in the value of <i>pfCancelled</i>.




## -see-also




<a href="https://msdn.microsoft.com/e742e381-0fd2-482a-81a0-7b43d11b073b">IActionProgress</a>



<a href="https://msdn.microsoft.com/28a2ee51-0a7a-4802-be55-f111be3a4d2d">IActionProgress::ResetCancel</a>
 

 

