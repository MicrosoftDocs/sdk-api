---
UID: NS:mprapi._MPR_TRANSPORT_0
title: MPR_TRANSPORT_0 (mprapi.h)
description: The MPR_TRANSPORT_0 structure contains information for a particular transport.
helpviewer_keywords: ["*PMPR_TRANSPORT_0","MPR_TRANSPORT_0","MPR_TRANSPORT_0 structure [RAS]","PMPR_TRANSPORT_0","PMPR_TRANSPORT_0 structure pointer [RAS]","_mpr_mpr_transport_0","mprapi/MPR_TRANSPORT_0","mprapi/PMPR_TRANSPORT_0","rras.mpr_transport_0"]
old-location: rras\mpr_transport_0.htm
tech.root: RRAS
ms.assetid: f5515a39-377d-4767-b508-2306832d81f7
ms.date: 12/05/2018
ms.keywords: '*PMPR_TRANSPORT_0, MPR_TRANSPORT_0, MPR_TRANSPORT_0 structure [RAS], PMPR_TRANSPORT_0, PMPR_TRANSPORT_0 structure pointer [RAS], _mpr_mpr_transport_0, mprapi/MPR_TRANSPORT_0, mprapi/PMPR_TRANSPORT_0, rras.mpr_transport_0'
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
req.typenames: MPR_TRANSPORT_0, *PMPR_TRANSPORT_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_TRANSPORT_0
 - mprapi/_MPR_TRANSPORT_0
 - PMPR_TRANSPORT_0
 - mprapi/PMPR_TRANSPORT_0
 - MPR_TRANSPORT_0
 - mprapi/MPR_TRANSPORT_0
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
 - MPR_TRANSPORT_0
---

# MPR_TRANSPORT_0 structure


## -description

The 
<b>MPR_TRANSPORT_0</b> structure contains information for a particular transport.

## -struct-fields

### -field dwTransportId

A <b>DWORD</b> value that identifies the transport protocol type. Supported transport protocol types are listed on <a href="/windows/desktop/RRAS/transport-identifiers">Transport Identifiers</a>.

### -field hTransport

Handle to the transport.

### -field wszTransportName

A Unicode string that contains the name of the transport.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_iftransport_0">MPR_IFTRANSPORT_0</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>