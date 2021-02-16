---
UID: NS:mprapi.RAS_UPDATE_CONNECTION_
title: RAS_UPDATE_CONNECTION (mprapi.h)
description: Used to update an active RAS connection.
helpviewer_keywords: ["*PRAS_UPDATE_CONNECTION","PRAS_UPDATE_CONNECTION","PRAS_UPDATE_CONNECTION structure pointer [RAS]","RAS_UPDATE_CONNECTION","RAS_UPDATE_CONNECTION structure [RAS]","mprapi/PRAS_UPDATE_CONNECTION","mprapi/RAS_UPDATE_CONNECTION","rras.ras_update_connection"]
old-location: rras\ras_update_connection.htm
tech.root: RRAS
ms.assetid: bfa35f1c-e9f5-43f1-ad2d-d54f4675cff8
ms.date: 12/05/2018
ms.keywords: '*PRAS_UPDATE_CONNECTION, PRAS_UPDATE_CONNECTION, PRAS_UPDATE_CONNECTION structure pointer [RAS], RAS_UPDATE_CONNECTION, RAS_UPDATE_CONNECTION structure [RAS], mprapi/PRAS_UPDATE_CONNECTION, mprapi/RAS_UPDATE_CONNECTION, rras.ras_update_connection'
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
req.typenames: RAS_UPDATE_CONNECTION, *PRAS_UPDATE_CONNECTION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RAS_UPDATE_CONNECTION_
 - mprapi/RAS_UPDATE_CONNECTION_
 - PRAS_UPDATE_CONNECTION
 - mprapi/PRAS_UPDATE_CONNECTION
 - RAS_UPDATE_CONNECTION
 - mprapi/RAS_UPDATE_CONNECTION
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
 - RAS_UPDATE_CONNECTION
---

# RAS_UPDATE_CONNECTION structure


## -description

The <a href="/previous-versions/windows/desktop/legacy/dd408110(v=vs.85)">RAS_UPDATE_CONNECTION</a> structure is  used to update an active RAS connection.

## -struct-fields

### -field Header

A <a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_object_header">MPRAPI_OBJECT_HEADER</a> structure that specifies the version of the <a href="/previous-versions/windows/desktop/legacy/dd408110(v=vs.85)">RAS_UPDATE_CONNECTION</a> structure. 

<div class="alert"><b>Note</b>  The <b>revision</b> member  of  <b>Header</b> must be <b>0x01</b> and <b>type</b> must be <b>MPRAPI_OBJECT_TYPE_UPDATE_CONNECTION_OBJECT</b>.</div>
<div> </div>

### -field dwIfIndex

A value that specifies the new interface index of the Virtual Private Network (VPN) endpoint.

### -field wszLocalEndpointAddress

A null-terminated Unicode string that contains the new IP address of the local computer in the connection. This string is of the form "a.b.c.d".

### -field wszRemoteEndpointAddress

A null-terminated Unicode string that contains the new IP address of the remote computer in the connection. This string is of the form "a.b.d.c".

## -see-also

<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>