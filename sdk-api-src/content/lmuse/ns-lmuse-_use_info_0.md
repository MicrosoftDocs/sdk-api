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

# _USE_INFO_0 structure


## -description


The
				<b>USE_INFO_0</b> structure contains the name of a shared resource and the local device redirected to it.


## -struct-fields




### -field ui0_local

Pointer to a Unicode string that specifies the local device name (for example, drive E or LPT1) being redirected to the shared resource. The constant DEVLEN specifies the maximum number of characters in the string.


### -field ui0_remote

Pointer to a Unicode string that specifies the share name of the remote resource being accessed. The string is in the form: 




<pre class="syntax" xml:space="preserve"><code>\\servername\sharename
</code></pre>

## -see-also




<a href="https://msdn.microsoft.com/fb527f85-baea-48e8-b837-967870834ec5">NetUseEnum</a>



<a href="https://msdn.microsoft.com/257875db-5ed9-4569-8dbb-5dcc7a6af95c">NetUseGetInfo</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>



<a href="https://msdn.microsoft.com/a4b05054-bef2-4cab-89f6-725d92ee75b8">Network Management Structures</a>



<a href="https://msdn.microsoft.com/ddf1b8dc-f13b-402a-9e4e-e4944a29ac31">Use Functions</a>
 

 

