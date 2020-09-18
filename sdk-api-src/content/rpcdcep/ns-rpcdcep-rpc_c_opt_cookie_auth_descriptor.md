---
UID: NS:rpcdcep._RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
title: RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR (rpcdcep.h)
description: The RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure contains a cookie that is inserted into the header of RPC/HTTP traffic.
helpviewer_keywords: ["PRPC_C_OPT_COOKIE_AUTH_DESCRIPTOR","PRPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure pointer [RPC]","RPC_CALL_ATTRIBUTES_V1_A","RPC_CALL_ATTRIBUTES_V1_W","RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR","RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure [RPC]","rpc.rpc_c_opt_cookie_auth_descriptor","rpcdcep/PRPC_C_OPT_COOKIE_AUTH_DESCRIPTOR","rpcdcep/RPC_CALL_ATTRIBUTES_V1_A","rpcdcep/RPC_CALL_ATTRIBUTES_V1_W","rpcdcep/RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR"]
old-location: rpc\rpc_c_opt_cookie_auth_descriptor.htm
tech.root: Rpc
ms.assetid: 808fdf38-4b54-42ab-855c-da9f2081214a
ms.date: 12/05/2018
ms.keywords: PRPC_C_OPT_COOKIE_AUTH_DESCRIPTOR, PRPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure pointer [RPC], RPC_CALL_ATTRIBUTES_V1_A, RPC_CALL_ATTRIBUTES_V1_W, RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR, RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure [RPC], rpc.rpc_c_opt_cookie_auth_descriptor, rpcdcep/PRPC_C_OPT_COOKIE_AUTH_DESCRIPTOR, rpcdcep/RPC_CALL_ATTRIBUTES_V1_A, rpcdcep/RPC_CALL_ATTRIBUTES_V1_W, rpcdcep/RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
req.header: rpcdcep.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RPC_CALL_ATTRIBUTES_V1_W (Unicode) and RPC_CALL_ATTRIBUTES_V1_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
 - rpcdcep/_RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
 - RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
 - rpcdcep/RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcdcep.h
api_name:
 - RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
 - RPC_CALL_ATTRIBUTES_V1_A
 - RPC_CALL_ATTRIBUTES_V1_W
---

# RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure


## -description

The <b>RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR</b> structure contains a cookie that is inserted into the header of RPC/HTTP traffic. This cookie can be used for authentication or for load balancing. When used for authentication, <a href="/windows/desktop/Debug/system-error-codes--1700-3999-">RPC_S_COOKIE_AUTH_FAILED</a>  is returned from an RPC call if cookie authentication fails. There are no specific error messages when used for load balancing.

## -struct-fields

### -field BufferSize

The length, in bytes, of <b>Buffer</b>.

### -field Buffer

A null-terminated string that contains the cookie.

## -remarks

A pointer to this structure is passed as the OptionValue when making a call to <a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption">RpcBindingSetOption</a>  with <a href="/windows/desktop/Rpc/binding-option-constants">RPC_C_OPT_COOKIE_AUTH</a>  as the option.