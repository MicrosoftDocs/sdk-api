---
UID: NS:mprapi._PPP_NBFCP_INFO
title: PPP_NBFCP_INFO (mprapi.h)
description: The PPP_NBFCP_INFO structure contains the result of a PPP NetBEUI Framer (NBF) projection operation.
helpviewer_keywords: ["PPP_NBFCP_INFO","PPP_NBFCP_INFO structure [RAS]","_mpr_ppp_nbfcp_info","mprapi/PPP_NBFCP_INFO","rras.ppp_nbfcp_info"]
old-location: rras\ppp_nbfcp_info.htm
tech.root: RRAS
ms.assetid: 376c662d-c0e1-4136-937c-47a4681c14ec
ms.date: 12/05/2018
ms.keywords: PPP_NBFCP_INFO, PPP_NBFCP_INFO structure [RAS], _mpr_ppp_nbfcp_info, mprapi/PPP_NBFCP_INFO, rras.ppp_nbfcp_info
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
req.typenames: PPP_NBFCP_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PPP_NBFCP_INFO
 - mprapi/_PPP_NBFCP_INFO
 - PPP_NBFCP_INFO
 - mprapi/PPP_NBFCP_INFO
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
 - PPP_NBFCP_INFO
---

# PPP_NBFCP_INFO structure


## -description

The 
<b>PPP_NBFCP_INFO</b> structure contains the result of a PPP NetBEUI Framer (NBF) projection operation.

## -struct-fields

### -field dwError

Specifies the result of the PPP control protocol negotiation. A value of zero indicates success. A nonzero value indicates failure, and is the actual fatal error that occurred during the control protocol negotiation.

### -field wszWksta

Specifies a Unicode string that is the local workstation's computer name. This unique computer name is the closest NetBIOS equivalent to a client's NetBEUI address on a remote access connection.

## -remarks

The 
<b>PPP_NBFCP_INFO</b> structure can be used only when administrating computers that are running an operating system prior to Windows Server 2003 as later operating systems do not support the NetBEUI protocol.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_info">PPP_INFO</a>



<a href="/windows/desktop/RRAS/ras-administration-structures">RAS Administration Structures</a>



<a href="/windows/desktop/RRAS/remote-access-service-administration-reference">Remote Access Service Administration Reference</a>