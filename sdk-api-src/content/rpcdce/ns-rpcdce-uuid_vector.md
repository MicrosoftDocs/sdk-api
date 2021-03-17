---
UID: NS:rpcdce._UUID_VECTOR
title: UUID_VECTOR (rpcdce.h)
description: The UUID_VECTOR structure contains a list of UUIDs.
helpviewer_keywords: ["UUID_VECTOR","UUID_VECTOR structure [RPC]","_rpc_uuid_vector","rpc.uuid_vector","rpcdce/UUID_VECTOR"]
old-location: rpc\uuid_vector.htm
tech.root: Rpc
ms.assetid: 6fc7216b-023b-4aca-a572-35cc22202522
ms.date: 12/05/2018
ms.keywords: UUID_VECTOR, UUID_VECTOR structure [RPC], _rpc_uuid_vector, rpc.uuid_vector, rpcdce/UUID_VECTOR
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
req.typenames: UUID_VECTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _UUID_VECTOR
 - rpcdce/_UUID_VECTOR
 - UUID_VECTOR
 - rpcdce/UUID_VECTOR
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
 - UUID_VECTOR
---

# UUID_VECTOR structure


## -description

The 
<b>UUID_VECTOR</b> structure contains a list of <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>s.

## -struct-fields

### -field Count

Number of <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>s present in the array <b>Uuid</b>.

### -field Uuid

Array of pointers to <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a>s that contains <b>Count</b> elements.

## -remarks

The <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> vector contains a count member containing the total number of <b>UUID</b>s in the vector, followed by an array of pointers to <b>UUID</b>s.

An application constructs a <a href="/windows/win32/rpc/rpcdce/ns-rpcdce-uuid">UUID</a> vector to contain object <b>UUID</b>s to be exported or unexported from the name service.

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregister">RpcEpRegister</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepregisternoreplace">RpcEpRegisterNoReplace</a>



<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcepunregister">RpcEpUnregister</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingexporta">RpcNsBindingExport</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingunexporta">RpcNsBindingUnexport</a>