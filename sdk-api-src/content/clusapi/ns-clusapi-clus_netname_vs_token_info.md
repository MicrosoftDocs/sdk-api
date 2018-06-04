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

# CLUS_NETNAME_VS_TOKEN_INFO structure


## -description


Contains the data needed to request a token. It is used as the input parameter of the <a href="https://msdn.microsoft.com/7a1033be-1b97-49d6-91f3-78f5efed1f4b">CLUSCTL_RESOURCE_NETNAME_GET_VIRTUAL_SERVER_TOKEN</a> control code.


## -struct-fields




### -field ProcessID

Process ID of the process requesting the token.


### -field DesiredAccess

Specifies an access mask that specifies the requested types of access. For a list of access rights for access 
      tokens, see 
      <a href="https://msdn.microsoft.com/5f710fd8-33de-47c0-a8b2-baf3008c4ed7">Access Rights for Access-Token Objects</a>.


### -field InheritHandle

Indicates whether the new handle is inheritable. If <b>TRUE</b>, the duplicate handle can 
      be inherited by new processes created by the target process. If <b>FALSE</b>, the new handle 
      cannot be inherited.


## -see-also




<a href="https://msdn.microsoft.com/7a1033be-1b97-49d6-91f3-78f5efed1f4b">CLUSCTL_RESOURCE_NETNAME_GET_VIRTUAL_SERVER_TOKEN</a>



<a href="https://msdn.microsoft.com/e3ad7c34-0c8a-4f03-8e5c-b57802c493f0">Data Structures</a>
 

 

