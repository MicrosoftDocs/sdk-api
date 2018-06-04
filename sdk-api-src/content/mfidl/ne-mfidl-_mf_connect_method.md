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

# _MF_CONNECT_METHOD enumeration


## -description


Specifies how the topology loader connects a topology node. This enumeration is used with the <a href="https://msdn.microsoft.com/8d70e1af-607b-47c3-9808-091c95fd05b7">MF_TOPONODE_CONNECT_METHOD</a> attribute.
        
      


## -enum-fields




### -field MF_CONNECT_DIRECT


            Connect the node directly to its upstream neighbor. Fail otherwise.
          


### -field MF_CONNECT_ALLOW_CONVERTER


            Add a converter transform upstream from this node, if needed to complete the connection. Converter transforms include color-space converters for video, and audio resamplers for audio.
          


### -field MF_CONNECT_ALLOW_DECODER


            Add a decoder transform upstream upstream from this node, if needed to complete the connection. The numeric value of this flag includes the <b>MF_CONNECT_ALLOW_CONVERTER</b> flag. Therefore, setting the <b>MF_CONNECT_ALLOW_DECODER</b> flag sets the <b>MF_CONNECT_ALLOW_CONVERTER</b> flag as well.
          


### -field MF_CONNECT_RESOLVE_INDEPENDENT_OUTPUTTYPES

Controls the order in which the topology loader attempts to  
            use different output types from this node. Currently, this flag applies only to source nodes. For more information, see <a href="https://msdn.microsoft.com/2675ef16-2018-47e8-bb22-2fc0d62e6681">MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES</a>. 

<div class="alert"><b>Note</b>  Requires Windows 7 or later.</div>
<div> </div>

### -field MF_CONNECT_AS_OPTIONAL


            This node is optional. If the topology loader cannot connect this node, it will skip the node and continue.
          


### -field MF_CONNECT_AS_OPTIONAL_BRANCH


            The entire topology branch starting at this node is optional. If the topology loader cannot resolve this branch, it will skip the branch and continue.
          


## -see-also




<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

