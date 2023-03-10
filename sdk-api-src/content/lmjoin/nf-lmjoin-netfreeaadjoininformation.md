---
UID: NF:lmjoin.NetFreeAadJoinInformation
title: NetFreeAadJoinInformation function (lmjoin.h)
description: Frees the memory allocated for the specified DSREG_JOIN_INFO structure, which contains join information for a tenant and which you retrieved by calling the NetGetAadJoinInformation function.
helpviewer_keywords: ["NetFreeAadJoinInformation","NetFreeAadJoinInformation function [Network Management]","lmjoin/NetFreeAadJoinInformation","netmgmt.netfreeaadjoininformation"]
old-location: netmgmt\netfreeaadjoininformation.htm
tech.root: NetMgmt
ms.assetid: BDFB6179-4B8C-43E3-8D34-A2B470EA0D0B
ms.date: 12/05/2018
ms.keywords: NetFreeAadJoinInformation, NetFreeAadJoinInformation function [Network Management], lmjoin/NetFreeAadJoinInformation, netmgmt.netfreeaadjoininformation
req.header: lmjoin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetFreeAadJoinInformation
 - lmjoin/NetFreeAadJoinInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - netapi32.dll
api_name:
 - NetFreeAadJoinInformation
---

# NetFreeAadJoinInformation function


## -description

Frees the memory allocated for the specified <a href="/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info">DSREG_JOIN_INFO</a> structure, which contains join information for a tenant and which you retrieved by calling the <a href="/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation">NetGetAadJoinInformation</a> function.

## -parameters

### -param pJoinInfo [in, optional]

Pointer to the <a href="/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info">DSREG_JOIN_INFO</a> structure for which you want to free the memory.

## -returns

This function does not return a value.

## -see-also

<a href="/windows/desktop/api/lmjoin/ns-lmjoin-dsreg_join_info">DSREG_JOIN_INFO</a>



<a href="/windows/desktop/api/lmjoin/nf-lmjoin-netgetaadjoininformation">NetGetAadJoinInformation</a>