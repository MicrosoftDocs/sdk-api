---
UID: NS:mprapi._PROJECTION_INFO2
title: PROJECTION_INFO2 (mprapi.h)
description: Used in the RAS_CONNECTION_4 structure as a placeholder for the PPP_PROJECTION_INFO2 and IKEV2_PROJECTION_INFO2 structures.
helpviewer_keywords: ["*PPROJECTION_INFO2","MPRAPI_IKEV2_PROJECTION_INFO_TYPE","MPRAPI_PPP_PROJECTION_INFO_TYPE","PPROJECTION_INFO2","PPROJECTION_INFO2 structure pointer [RAS]","PROJECTION_INFO2","PROJECTION_INFO2 structure [RAS]","mprapi/PPROJECTION_INFO2","mprapi/PROJECTION_INFO2","rras.projection_info2"]
old-location: rras\projection_info2.htm
tech.root: RRAS
ms.assetid: 820acc2b-38e1-4501-9753-bc250d6a87c9
ms.date: 12/05/2018
ms.keywords: '*PPROJECTION_INFO2, MPRAPI_IKEV2_PROJECTION_INFO_TYPE, MPRAPI_PPP_PROJECTION_INFO_TYPE, PPROJECTION_INFO2, PPROJECTION_INFO2 structure pointer [RAS], PROJECTION_INFO2, PROJECTION_INFO2 structure [RAS], mprapi/PPROJECTION_INFO2, mprapi/PROJECTION_INFO2, rras.projection_info2'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: PROJECTION_INFO2, *PPROJECTION_INFO2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PROJECTION_INFO2
 - mprapi/_PROJECTION_INFO2
 - PPROJECTION_INFO2
 - mprapi/PPROJECTION_INFO2
 - PROJECTION_INFO2
 - mprapi/PROJECTION_INFO2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mprapi.h
api_name:
 - PROJECTION_INFO2
---

# PROJECTION_INFO2 structure


## -description

Used in the <a href="/windows/desktop/api/mprapi/ns-mprapi-ras_connection_4">RAS_CONNECTION_4</a> structure as a placeholder for the <a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_projection_info2">PPP_PROJECTION_INFO2</a> and <a href="/windows/desktop/api/mprapi/ns-mprapi-ikev2_projection_info2">IKEV2_PROJECTION_INFO2</a> structures.

## -struct-fields

### -field projectionInfoType

A value that specifies if the projection is for a Point-to-Point (PPP) or an Internet Key Exchange version 2 (IKEv2) based tunnel. The following values are supported.

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
The data is a <a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_projection_info2">PPP_PROJECTION_INFO2</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="MPRAPI_IKEV2_PROJECTION_INFO_TYPE"></a><a id="mprapi_ikev2_projection_info_type"></a><dl>
<dt><b>MPRAPI_IKEV2_PROJECTION_INFO_TYPE</b></dt>
</dl>
</td>
<td width="60%">
The data is a <a href="/windows/desktop/api/mprapi/ns-mprapi-ikev2_projection_info2">IKEV2_PROJECTION_INFO2</a> structure.

</td>
</tr>
</table>

### -field PppProjectionInfo

A <a href="/windows/desktop/api/mprapi/ns-mprapi-ppp_projection_info2">PPP_PROJECTION_INFO2</a> structure that is used for a PPP based tunnel.

### -field Ikev2ProjectionInfo

A <a href="/windows/desktop/api/mprapi/ns-mprapi-ikev2_projection_info2">IKEV2_PROJECTION_INFO2</a> structure that is used for an IKEv2 based tunnel.