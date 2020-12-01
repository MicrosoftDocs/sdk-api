---
UID: NS:mprapi._PROJECTION_INFO
title: PROJECTION_INFO (mprapi.h)
description: Is used in the RAS_CONNECTION_EX structure as a placeholder for the PPP_PROJECTION_INFO and IKEV2_PROJECTION_INFO structures.
helpviewer_keywords: ["*PPROJECTION_INFO","MPRAPI_IKEV2_PROJECTION_INFO_TYPE","MPRAPI_PPP_PROJECTION_INFO_TYPE","PPROJECTION_INFO","PPROJECTION_INFO structure pointer [RAS]","PROJECTION_INFO","PROJECTION_INFO structure [RAS]","mprapi/PPROJECTION_INFO","mprapi/PROJECTION_INFO","rras.projection_info"]
old-location: rras\projection_info.htm
tech.root: RRAS
ms.assetid: 3f87d09a-2408-4fe4-97f9-61ed9b5d2fa5
ms.date: 12/05/2018
ms.keywords: '*PPROJECTION_INFO, MPRAPI_IKEV2_PROJECTION_INFO_TYPE, MPRAPI_PPP_PROJECTION_INFO_TYPE, PPROJECTION_INFO, PPROJECTION_INFO structure pointer [RAS], PROJECTION_INFO, PROJECTION_INFO structure [RAS], mprapi/PPROJECTION_INFO, mprapi/PROJECTION_INFO, rras.projection_info'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: PROJECTION_INFO, *PPROJECTION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROJECTION_INFO
 - mprapi/_PROJECTION_INFO
 - PPROJECTION_INFO
 - mprapi/PPROJECTION_INFO
 - PROJECTION_INFO
 - mprapi/PROJECTION_INFO
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
 - PROJECTION_INFO
---

# PROJECTION_INFO structure


## -description

The <b>PROJECTION_INFO</b> structure  is used in the <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a> structure as a placeholder for  the <a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_projection_info">PPP_PROJECTION_INFO</a>  and <a href="/windows/desktop/api/mprapi/ns-mprapi-ikev2_projection_info">IKEV2_PROJECTION_INFO</a> structures.

## -struct-fields

### -field projectionInfoType

A value that specifies if the projection is for a Point-to-Point (PPP) or an Internet Key Exchange version 2 (IKEv2) based tunnel. The following values are supported:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_PPP_PROJECTION_INFO_TYPE"></a><a id="mprapi_ppp_projection_info_type"></a><dl>
<dt><b>MPRAPI_PPP_PROJECTION_INFO_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Data is a <a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_projection_info">PPP_PROJECTION_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_IKEV2_PROJECTION_INFO_TYPE"></a><a id="mprapi_ikev2_projection_info_type"></a><dl>
<dt><b>MPRAPI_IKEV2_PROJECTION_INFO_TYPE</b></dt>
</dl>
</td>
<td width="60%">
Data is a <a href="/windows/desktop/api/mprapi/ns-mprapi-ikev2_projection_info">IKEV2_PROJECTION_INFO</a> structure.

</td>
</tr>
</table>

### -field PppProjectionInfo

A <a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_projection_info">PPP_PROJECTION_INFO</a> structure that is used for a PPP based tunnel.

### -field Ikev2ProjectionInfo

A <a href="/windows/desktop/api/mprapi/ns-mprapi-ikev2_projection_info">IKEV2_PROJECTION_INFO</a> structure that is used for an IKEv2 based tunnel.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_ex">RAS_CONNECTION_EX</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>