---
UID: NS:rpcndr._NDR_USER_MARSHAL_INFO
title: NDR_USER_MARSHAL_INFO (rpcndr.h)
description: The NDR_USER_MARSHAL_INFO structure holds information about the state of an RPC call that can be passed to wire_marshal and user_marshal helper functions.
helpviewer_keywords: ["NDR_USER_MARSHAL_INFO","NDR_USER_MARSHAL_INFO structure [RPC]","_rpc_ndr_user_marshal_info","rpc.ndr_user_marshal_info","rpcndr/NDR_USER_MARSHAL_INFO"]
old-location: rpc\ndr_user_marshal_info.htm
tech.root: Rpc
ms.assetid: 3c7b4cd4-fb72-40a6-9450-4edf82cade2c
ms.date: 12/05/2018
ms.keywords: NDR_USER_MARSHAL_INFO, NDR_USER_MARSHAL_INFO structure [RPC], _rpc_ndr_user_marshal_info, rpc.ndr_user_marshal_info, rpcndr/NDR_USER_MARSHAL_INFO
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
targetos: Windows
req.typenames: NDR_USER_MARSHAL_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NDR_USER_MARSHAL_INFO
 - rpcndr/_NDR_USER_MARSHAL_INFO
 - NDR_USER_MARSHAL_INFO
 - rpcndr/NDR_USER_MARSHAL_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcndr.h
api_name:
 - NDR_USER_MARSHAL_INFO
---

# NDR_USER_MARSHAL_INFO structure


## -description

The 
<b>NDR_USER_MARSHAL_INFO</b> structure holds information about the state of an RPC call that can be passed to 
<a href="/windows/desktop/Midl/wire-marshal">wire_marshal</a> and 
<a href="/windows/desktop/Midl/user-marshal">user_marshal</a> helper functions.

## -struct-fields

### -field InformationLevel

The information level of the returned data. Currently only a value of 1 is defined.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.Level1

An 
<a href="/windows/desktop/api/rpcndr/ns-rpcndr-ndr_user_marshal_info_level1">NDR_USER_MARSHAL_INFO_LEVEL1</a> structure.

## -remarks

The function 
<a href="/windows/desktop/api/rpcndr/nf-rpcndr-ndrgetusermarshalinfo">NdrGetUserMarshalInfo</a> fills this structure with supplemental information for the 
<a href="/windows/desktop/Midl/user-marshal">user_marshal</a> and 
<a href="/windows/desktop/Midl/wire-marshal">wire_marshal</a> helper functions &lt;type&gt;_UserSize, &lt;type&gt;_UserMarshal, &lt;type&gt;_UserUnmarshal, and &lt;type&gt;_UserFree. This information supplements the <i>pFlags</i> parameter that is passed to these helper functions. Not all of these fields will contain valid information in all contexts. Level1.pRpcChannelBuffer is only valid for COM interfaces, and the buffer fields are only valid when 
<b>NdrGetUserMarshalInfo</b> is called from &lt;type&gt;_UserMarshal or &lt;type&gt;_UserUnmarshal.
