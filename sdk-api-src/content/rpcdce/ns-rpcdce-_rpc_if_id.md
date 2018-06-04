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

# _RPC_IF_ID structure


## -description


The 
<b>RPC_IF_ID</b> structure contains the interface UUID and major and minor version numbers of an interface.


## -struct-fields




### -field Uuid

Specifies the interface 
<a href="midl.uuid">UUID</a>.


### -field VersMajor

Major version number, an integer from 0 to 65535, inclusive.


### -field VersMinor

Minor version number, an integer from 0 to 65535, inclusive.


## -remarks



An interface identification is a subset of the data contained in the interface-specification structure. Routines that require an interface identification structure show a data type of 
<b>RPC_IF_ID</b>. In those routines, the application is responsible for providing memory for the structure.




## -see-also




<a href="https://msdn.microsoft.com/1b91e88c-b242-472f-b719-60f96599cb67">RpcIfInqId</a>
 

 

