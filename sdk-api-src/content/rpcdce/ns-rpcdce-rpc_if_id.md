---
UID: NS:rpcdce._RPC_IF_ID
title: RPC_IF_ID (rpcdce.h)
description: The RPC_IF_ID structure contains the interface UUID and major and minor version numbers of an interface.
helpviewer_keywords: ["RPC_IF_ID","RPC_IF_ID structure [RPC]","_rpc_rpc_if_id","rpc.rpc_if_id","rpcdce/RPC_IF_ID"]
old-location: rpc\rpc_if_id.htm
tech.root: Rpc
ms.assetid: 6fad80e0-4239-48f7-9cd1-3b9c56303346
ms.date: 12/05/2018
ms.keywords: RPC_IF_ID, RPC_IF_ID structure [RPC], _rpc_rpc_if_id, rpc.rpc_if_id, rpcdce/RPC_IF_ID
req.header: rpcdce.h
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
req.typenames: RPC_IF_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_IF_ID
 - rpcdce/_RPC_IF_ID
 - RPC_IF_ID
 - rpcdce/RPC_IF_ID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdce.h
api_name:
 - RPC_IF_ID
---

# RPC_IF_ID structure


## -description

The 
<b>RPC_IF_ID</b> structure contains the interface UUID and major and minor version numbers of an interface.

## -struct-fields

### -field Uuid

Specifies the interface 
<a href="https://msdn.microsoft.com/">UUID</a>.

### -field VersMajor

Major version number, an integer from 0 to 65535, inclusive.

### -field VersMinor

Minor version number, an integer from 0 to 65535, inclusive.

## -remarks

An interface identification is a subset of the data contained in the interface-specification structure. Routines that require an interface identification structure show a data type of 
<b>RPC_IF_ID</b>. In those routines, the application is responsible for providing memory for the structure.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcifinqid">RpcIfInqId</a>