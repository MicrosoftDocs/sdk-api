---
UID: NS:rpcdce.RPC_ENDPOINT_TEMPLATEA
title: RPC_ENDPOINT_TEMPLATEA (rpcdce.h)
description: Specifies the properties of an RPC interface group server endpoint, including protocol sequence and name. (RPC_ENDPOINT_TEMPLATEA)
helpviewer_keywords: ["*PRPC_ENDPOINT_TEMPLATEA","PRPC_ENDPOINT_TEMPLATE","PRPC_ENDPOINT_TEMPLATE structure pointer [RPC]","RPC_ENDPOINT_TEMPLATE","RPC_ENDPOINT_TEMPLATE structure [RPC]","RPC_ENDPOINT_TEMPLATEA","RPC_ENDPOINT_TEMPLATEW","rpc.rpc_endpoint_template","rpcdce/PRPC_ENDPOINT_TEMPLATE","rpcdce/RPC_ENDPOINT_TEMPLATE","rpcdce/RPC_ENDPOINT_TEMPLATEA","rpcdce/RPC_ENDPOINT_TEMPLATEW"]
old-location: rpc\rpc_endpoint_template.htm
tech.root: Rpc
ms.assetid: F1C4A10B-D7DA-4A2A-B166-F814E6926ADD
ms.date: 12/05/2018
ms.keywords: '*PRPC_ENDPOINT_TEMPLATEA, PRPC_ENDPOINT_TEMPLATE, PRPC_ENDPOINT_TEMPLATE structure pointer [RPC], RPC_ENDPOINT_TEMPLATE, RPC_ENDPOINT_TEMPLATE structure [RPC], RPC_ENDPOINT_TEMPLATEA, RPC_ENDPOINT_TEMPLATEW, rpc.rpc_endpoint_template, rpcdce/PRPC_ENDPOINT_TEMPLATE, rpcdce/RPC_ENDPOINT_TEMPLATE, rpcdce/RPC_ENDPOINT_TEMPLATEA, rpcdce/RPC_ENDPOINT_TEMPLATEW'
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RPC_ENDPOINT_TEMPLATEW (Unicode) and RPC_ENDPOINT_TEMPLATEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_ENDPOINT_TEMPLATEA, *PRPC_ENDPOINT_TEMPLATEA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PRPC_ENDPOINT_TEMPLATEA
 - rpcdce/PRPC_ENDPOINT_TEMPLATEA
 - RPC_ENDPOINT_TEMPLATEA
 - rpcdce/RPC_ENDPOINT_TEMPLATEA
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
 - RPC_ENDPOINT_TEMPLATE
 - RPC_ENDPOINT_TEMPLATEA
 - RPC_ENDPOINT_TEMPLATEW
---

# RPC_ENDPOINT_TEMPLATEA structure


## -description

The <b>RPC_ENDPOINT_TEMPLATE</b> structure specifies the properties of an RPC interface group server endpoint, including protocol sequence and name.

## -struct-fields

### -field Version

This field is reserved and must be set to 0.

### -field ProtSeq

Pointer to a string identifier of the protocol sequence to register with the RPC run-time library.  Only <a href="/windows/desktop/Rpc/protocol-sequence-constants">ncalrpc</a>, ncacn_ip_tcp, and ncacn_np are supported.  This value must not be <b>NULL</b>.

### -field Endpoint

Optional pointer to the endpoint-address information to use in creating a binding for the protocol sequence specified in the <i>Protseq</i> parameter.  Specify <b>NULL</b> to use dynamic endpoints.

### -field SecurityDescriptor

Pointer to an optional parameter provided for the security subsystem. Used only for <a href="/windows/desktop/Rpc/protocol-sequence-constants">ncacn_np</a> and ncalrpc protocol sequences. All other protocol sequences ignore this parameter. Using a security descriptor on the endpoint in order to make a server secure is not recommended.

### -field Backlog

Backlog queue length for the <a href="/windows/desktop/Rpc/protocol-sequence-constants">ncacn_ip_tcp</a> protocol sequence. All other protocol sequences ignore this parameter. Use <b>RPC_C_PROTSEQ_MAX_REQS_DEFAULT</b> to specify the default value.  See Remarks for more information.

## -remarks

The value provided in <i>Backlog</i> by applications is only a hint. The RPC run time or the Windows Sockets provider may override the value. For example, on Windows XP or Windows 2000 Professional, the value is limited to 5. Values greater than 5 are ignored and 5 is used instead. On Windows Server 2003 and Windows 2000 Server, the value will be honored.

Applications must be careful to pass reasonable values in <i>Backlog</i>. Large values on Server, Advanced Server, or Datacenter Server can cause a large amount of non-paged pool memory to be used. Using too small a value is also unfavorable, as it may result in TCP SYN packets being met by TCP RST from the server if the backlog queue gets exhausted.

An application developer should balance memory footprint versus scalability requirements when determining the proper value for <i>Backlog</i>.





> [!NOTE]
> The rpcdce.h header defines RPC_ENDPOINT_TEMPLATE as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverinterfacegroupinqbindings">RpcServerInqBindings</a>

