---
UID: NS:mprapi._MPR_SERVER_0
title: MPR_SERVER_0 (mprapi.h)
description: The MPR_SERVER_0 structure is used to retrieve information about a device.
helpviewer_keywords: ["*PMPR_SERVER_0","MPR_SERVER_0","MPR_SERVER_0 structure [RAS]","PMPR_SERVER_0","PMPR_SERVER_0 structure pointer [RAS]","_mpr_mpr_server_0","mprapi/MPR_SERVER_0","mprapi/PMPR_SERVER_0","rras.mpr_server_0"]
old-location: rras\mpr_server_0.htm
tech.root: RRAS
ms.assetid: cffda25b-28f8-4d76-987c-eadcea9c032b
ms.date: 12/05/2018
ms.keywords: '*PMPR_SERVER_0, MPR_SERVER_0, MPR_SERVER_0 structure [RAS], PMPR_SERVER_0, PMPR_SERVER_0 structure pointer [RAS], _mpr_mpr_server_0, mprapi/MPR_SERVER_0, mprapi/PMPR_SERVER_0, rras.mpr_server_0'
req.header: mprapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: MPR_SERVER_0, *PMPR_SERVER_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_SERVER_0
 - mprapi/_MPR_SERVER_0
 - PMPR_SERVER_0
 - mprapi/PMPR_SERVER_0
 - MPR_SERVER_0
 - mprapi/MPR_SERVER_0
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
 - MPR_SERVER_0
---

# MPR_SERVER_0 structure


## -description

The 
<b>MPR_SERVER_0</b> structure is used to retrieve information about a device.

## -struct-fields

### -field fLanOnlyMode

A <b>BOOL</b> that specifies whether the Demand Dial Manager (DDM) is running on the device. If <b>TRUE</b>, the DDM is not running on the device. Otherwise, it is <b>FALSE</b>.

### -field dwUpTime

Specifies the elapsed time, in seconds, since the device was started.

### -field dwTotalPorts

Specifies the number of ports on the device.

### -field dwPortsInUse

Specifies the number of ports currently in use on the device.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_1">MPR_SERVER_1</a>



<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_server_2">MPR_SERVER_2</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mpradminservergetinfo">MprAdminServerGetInfo</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfigservergetinfo">MprConfigServerGetInfo</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>