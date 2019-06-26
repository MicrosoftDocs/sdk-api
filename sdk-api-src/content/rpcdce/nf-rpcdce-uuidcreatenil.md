---
UID: NF:rpcdce.UuidCreateNil
title: UuidCreateNil function (rpcdce.h)
author: windows-sdk-content
description: The UuidCreateNil function creates a nil-valued UUID.
old-location: rpc\uuidcreatenil.htm
tech.root: Rpc
ms.assetid: ee955482-e786-4478-bbaa-7c574ab1ecc5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UuidCreateNil, UuidCreateNil function [RPC], _rpc_uuidcreatenil, rpc.uuidcreatenil, rpcdce/UuidCreateNil
ms.topic: function
f1_keywords: 
 - "rpcdce/UuidCreateNil"
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - UuidCreateNil
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UuidCreateNil function


## -description


The 
<b>UuidCreateNil</b> function creates a nil-valued <a href="https://docs.microsoft.com/previous-versions/aa379358(v=vs.80)">UUID</a>.


## -parameters




### -param NilUuid

Returns a nil-valued 
<a href="https://docs.microsoft.com/previous-versions/aa379358(v=vs.80)">UUID</a>.


## -returns



Returns RPC_S_OK.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-uuidcreate">UuidCreate</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-uuidfromstring">UuidFromString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring">UuidToString</a>
 

 

