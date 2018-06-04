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

# _NDR_USER_MARSHAL_INFO structure


## -description


The 
<b>NDR_USER_MARSHAL_INFO</b> structure holds information about the state of an RPC call that can be passed to 
<a href="midl.wire_marshal">wire_marshal</a> and 
<a href="midl.user_marshal">user_marshal</a> helper functions.


## -struct-fields




### -field InformationLevel

The information level of the returned data. Currently only a value of 1 is defined.


### -field DUMMYUNIONNAME

 


### -field DUMMYUNIONNAME.Level1

An 
<a href="https://msdn.microsoft.com/fe664968-ce70-4bc4-9caa-3e4d241d253c">NDR_USER_MARSHAL_INFO_LEVEL1</a> structure.


## -remarks



The function 
<a href="https://msdn.microsoft.com/772979eb-eb1c-4e41-91bf-f64766898c8a">NdrGetUserMarshalInfo</a> fills this structure with supplemental information for the 
<a href="midl.user_marshal">user_marshal</a> and 
<a href="midl.wire_marshal">wire_marshal</a> helper functions &lt;type&gt;_UserSize, &lt;type&gt;_UserMarshal, &lt;type&gt;_UserUnmarshal, and &lt;type&gt;_UserFree. This information supplements the <i>pFlags</i> parameter that is passed to these helper functions. Not all of these fields will contain valid information in all contexts. Level1.pRpcChannelBuffer is only valid for COM interfaces, and the buffer fields are only valid when 
<b>NdrGetUserMarshalInfo</b> is called from &lt;type&gt;_UserMarshal or &lt;type&gt;_UserUnmarshal.



