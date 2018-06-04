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

# ItsPubPlugin2::ResolvePersonalDesktop


## -description


Called to resolve a mapping between the specified user and a virtual machine in a personal virtual desktop collection.


## -parameters




### -param userId [in]

A null-terminated string that contains the security identifier (SID) of the user.


### -param poolId [in]

A null-terminated string that contains the identifier of the collection to obtain the personal desktop from or create the personal desktop in.


### -param ePdResolutionType [in]

A value of the <a href="https://msdn.microsoft.com/8cba4e6a-3508-4f9f-a206-4a0b41a933c1">TSPUB_PLUGIN_PD_RESOLUTION_TYPE</a> enumeration that specifies the type of resolution being requested.


### -param pPdAssignmentType [out]

A value of the <a href="https://msdn.microsoft.com/8a55d72c-215e-4f72-90dd-0f68c107a635">TSPUB_PLUGIN_PD_ASSIGNMENT_TYPE</a> enumeration that specifies what type of assignment was made for the personal desktop.


### -param endPointName [out]

A null-terminated string that receives the name of the end point for the desktop. The length of this string is limited to <b>MAX_ENDPOINT_SIZE</b> characters, including the terminating <b>NULL</b> character.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>MAX_ENDPOINT_SIZE</b> is declared as follows:

<code>#define MAX_ENDPOINT_SIZE 256</code>




## -see-also




<a href="https://msdn.microsoft.com/1ef27b3a-b897-4757-803d-d3a18959895c">ItsPubPlugin2</a>
 

 

