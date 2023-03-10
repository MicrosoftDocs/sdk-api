---
UID: NS:mprapi._MPR_SERVER_EX1
title: MPR_SERVER_EX1 (mprapi.h)
description: Used to get or set the configuration of a RAS server. (MPR_SERVER_EX1)
helpviewer_keywords: ["*PMPR_SERVER_EX1","MPR_SERVER_EX","MPR_SERVER_EX structure [RAS]","MPR_SERVER_EX0","MPR_SERVER_EX1","PMPR_SERVER_EX","PMPR_SERVER_EX structure pointer [RAS]","_MPR_SERVER_EX0","_MPR_SERVER_EX1","mprapi/MPR_SERVER_EX","mprapi/PMPR_SERVER_EX","rras.mpr_server_ex"]
old-location: rras\mpr_server_ex.htm
tech.root: RRAS
ms.assetid: 10c1e3bd-adb8-4aff-835c-e7d881c9f5cf
ms.date: 12/05/2018
ms.keywords: '*PMPR_SERVER_EX1, MPR_SERVER_EX, MPR_SERVER_EX structure [RAS], MPR_SERVER_EX0, MPR_SERVER_EX1, PMPR_SERVER_EX, PMPR_SERVER_EX structure pointer [RAS], _MPR_SERVER_EX0, _MPR_SERVER_EX1, mprapi/MPR_SERVER_EX, mprapi/PMPR_SERVER_EX, rras.mpr_server_ex'
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
req.typenames: MPR_SERVER_EX1, *PMPR_SERVER_EX1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_SERVER_EX1
 - mprapi/_MPR_SERVER_EX1
 - PMPR_SERVER_EX1
 - mprapi/PMPR_SERVER_EX1
 - MPR_SERVER_EX1
 - mprapi/MPR_SERVER_EX1
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
 - MPR_SERVER_EX
 - MPR_SERVER_EX0
 - MPR_SERVER_EX1
---

# MPR_SERVER_EX1 structure


## -description

The <b>MPR_SERVER_EX</b> structure is used to get or set the configuration of a RAS server.

## -struct-fields

### -field Header

A <a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_object_header">MPRAPI_OBJECT_HEADER</a> structure that specifies the version of the <b>MPR_SERVER_EX</b> structure. 

<div class="alert"><b>Note</b>  The <b>revision</b> member  of  <b>Header</b> must be <b>MPRAPI_MPR_SERVER_OBJECT_REVISION_1</b>  and <b>type</b> must be <b>MPRAPI_OBJECT_TYPE_MPR_SERVER_OBJECT</b>.</div>
<div> </div>

### -field fLanOnlyMode

A BOOL that is <b>TRUE</b> if the RRAS server is running in LAN-only mode and <b>FALSE</b> if it is functioning as a router.

### -field dwUpTime

A value that specifies the elapsed time, in seconds, since the RAS server was started.

### -field dwTotalPorts

A value that specifies the number of ports on the RAS server.

### -field dwPortsInUse

A value that specifies the number of ports currently in use on the RAS server.

### -field Reserved

Reserved. This value must be zero.

### -field ConfigParams

A <a href="/windows/desktop/api/mprapi/ns-mprapi-mprapi_tunnel_config_params0">MPRAPI_TUNNEL_CONFIG_PARAMS</a> structure that contains Point-to-Point (PPTP), Secure Socket Tunneling Protocol (SSTP), Layer 2 Tunneling Protocol (L2TP), and Internet Key version 2 (IKEv2) tunnel configuration information for the RAS server.

## -see-also

<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>
