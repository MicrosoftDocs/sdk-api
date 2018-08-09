---
UID: NS:rpcdcep._RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
title: "_RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR"
author: windows-sdk-content
description: The RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure contains a cookie that is inserted into the header of RPC/HTTP traffic.
old-location: rpc\rpc_c_opt_cookie_auth_descriptor.htm
old-project: rpc
ms.assetid: 808fdf38-4b54-42ab-855c-da9f2081214a
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PRPC_C_OPT_COOKIE_AUTH_DESCRIPTOR, PRPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure pointer [RPC], RPC_CALL_ATTRIBUTES_V1_A, RPC_CALL_ATTRIBUTES_V1_W, RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR, RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure [RPC], _RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR, rpc.rpc_c_opt_cookie_auth_descriptor, rpcdcep/PRPC_C_OPT_COOKIE_AUTH_DESCRIPTOR, rpcdcep/RPC_CALL_ATTRIBUTES_V1_A, rpcdcep/RPC_CALL_ATTRIBUTES_V1_W, rpcdcep/RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# _RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR structure


## -description


The <b>RPC_C_OPT_COOKIE_AUTH_DESCRIPTOR</b> structure contains a cookie that is inserted into the header of RPC/HTTP traffic. This cookie can be used for authentication or for load balancing. When used for authentication, <a href="https://msdn.microsoft.com/7e57c087-53e4-443d-9227-21d9eb3cc71f">RPC_S_COOKIE_AUTH_FAILED</a>  is returned from an RPC call if cookie authentication fails. There are no specific error messages when used for load balancing.


## -struct-fields




### -field BufferSize

The length, in bytes, of <b>Buffer</b>.


### -field Buffer

A null-terminated string that contains the cookie.


## -remarks



A pointer to this structure is passed as the OptionValue when making a call to <a href="https://msdn.microsoft.com/bc721fb0-2271-4658-995b-a41e8eefc5d5">RpcBindingSetOption</a>  with <a href="https://msdn.microsoft.com/ff88e05d-b9f3-42ef-a44f-fee9261832c8">RPC_C_OPT_COOKIE_AUTH</a>  as the option.



