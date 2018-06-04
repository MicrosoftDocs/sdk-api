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

# D2D1_PATCH_EDGE_MODE enumeration


## -description


Specifies how to render gradient mesh edges.


## -enum-fields




### -field D2D1_PATCH_EDGE_MODE_ALIASED

Render this patch edge aliased. Use this value for the internal edges of your gradient mesh.


### -field D2D1_PATCH_EDGE_MODE_ANTIALIASED

Render this patch edge antialiased. Use this value for the external (boundary) edges of your mesh.


### -field D2D1_PATCH_EDGE_MODE_ALIASED_INFLATED

Render this patch edge aliased and also slightly inflated. Use this for the internal edges of your gradient mesh when there could be t-junctions among patches. 
          Inflating the internal edges mitigates seams that can appear along those junctions.


### -field D2D1_PATCH_EDGE_MODE_FORCE_DWORD



