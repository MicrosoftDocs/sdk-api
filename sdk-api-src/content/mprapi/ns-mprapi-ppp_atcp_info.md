---
UID: NS:mprapi._PPP_ATCP_INFO
title: PPP_ATCP_INFO (mprapi.h)
description: The PPP_ATCP_INFO structure contains the result of a PPP AppleTalk projection operation.
helpviewer_keywords: ["PPP_ATCP_INFO","PPP_ATCP_INFO structure [RAS]","_mpr_ppp_atcp_info","mprapi/PPP_ATCP_INFO","rras.ppp_atcp_info"]
old-location: rras\ppp_atcp_info.htm
tech.root: RRAS
ms.assetid: 48d2404b-df8d-4ed0-9203-921474c88551
ms.date: 12/05/2018
ms.keywords: PPP_ATCP_INFO, PPP_ATCP_INFO structure [RAS], _mpr_ppp_atcp_info, mprapi/PPP_ATCP_INFO, rras.ppp_atcp_info
req.header: mprapi.h
req.include-header: 
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
req.typenames: PPP_ATCP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_ATCP_INFO
 - mprapi/_PPP_ATCP_INFO
 - PPP_ATCP_INFO
 - mprapi/PPP_ATCP_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mprapi.h
api_name:
 - PPP_ATCP_INFO
---

# PPP_ATCP_INFO structure


## -description

The 
<b>PPP_ATCP_INFO</b> structure contains the result of a PPP AppleTalk projection operation.

## -struct-fields

### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.

### -field wszAddress

Specifies a Unicode string that holds the client's AppleTalk address on the RAS connection.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info">PPP_INFO</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>