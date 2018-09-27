---
UID: NS:rpcndr._NDR_USER_MARSHAL_INFO
title: "_NDR_USER_MARSHAL_INFO"
author: windows-sdk-content
description: The NDR_USER_MARSHAL_INFO structure holds information about the state of an RPC call that can be passed to wire_marshal and user_marshal helper functions.
old-location: rpc\ndr_user_marshal_info.htm
tech.root: rpc
ms.assetid: 3c7b4cd4-fb72-40a6-9450-4edf82cade2c
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: NDR_USER_MARSHAL_INFO, NDR_USER_MARSHAL_INFO structure [RPC], _NDR_USER_MARSHAL_INFO, _rpc_ndr_user_marshal_info, rpc.ndr_user_marshal_info, rpcndr/NDR_USER_MARSHAL_INFO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcndr.h
api_name:
 - NDR_USER_MARSHAL_INFO
product: Windows
targetos: Windows
req.typenames: NDR_USER_MARSHAL_INFO
req.redist: 
---

# _NDR_USER_MARSHAL_INFO structure


## -description


The 
<b>NDR_USER_MARSHAL_INFO</b> structure holds information about the state of an RPC call that can be passed to 
<a href="https://msdn.microsoft.com/">wire_marshal</a> and 
<a href="https://msdn.microsoft.com/">user_marshal</a> helper functions.


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
<a href="https://msdn.microsoft.com/">user_marshal</a> and 
<a href="https://msdn.microsoft.com/">wire_marshal</a> helper functions &lt;type&gt;_UserSize, &lt;type&gt;_UserMarshal, &lt;type&gt;_UserUnmarshal, and &lt;type&gt;_UserFree. This information supplements the <i>pFlags</i> parameter that is passed to these helper functions. Not all of these fields will contain valid information in all contexts. Level1.pRpcChannelBuffer is only valid for COM interfaces, and the buffer fields are only valid when 
<b>NdrGetUserMarshalInfo</b> is called from &lt;type&gt;_UserMarshal or &lt;type&gt;_UserUnmarshal.



