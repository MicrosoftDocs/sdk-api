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

# _DFS_INFO_7 structure


## -description


Contains information about a DFS namespace. This structure contains the version 
    <b>GUID</b> for the metadata for the namespace.

This information level is available to DFS roots only.


## -struct-fields




### -field GenerationGuid

The value of this <b>GUID</b> changes each time the DFS metadata is changed.


## -remarks



This structure is used to detect when the metadata of a DFS namespace has changed. It is currently supported 
     only for  domain-based DFS namespace servers.

If a DFS namespace server does not support generation <b>GUID</b>s, the 
     <b>GUID</b> value returned by 
     <a href="https://msdn.microsoft.com/bbb2f24d-1c49-4016-a16b-60fde4a78193">NetDfsGetInfo</a> contains a null 
     <b>GUID</b> (all zeros). This structure cannot be used with 
     <a href="https://msdn.microsoft.com/065ec002-cb90-4d78-a70c-6ac37f71994f">NetDfsGetClientInfo</a>.



