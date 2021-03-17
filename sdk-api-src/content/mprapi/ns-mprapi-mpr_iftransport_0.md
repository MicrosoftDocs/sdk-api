---
UID: NS:mprapi._MPR_IFTRANSPORT_0
title: MPR_IFTRANSPORT_0 (mprapi.h)
description: The MPR_IFTRANSPORT_0 structure contains information for a particular interface transport.
helpviewer_keywords: ["*PMPR_IFTRANSPORT_0","MPR_IFTRANSPORT_0","MPR_IFTRANSPORT_0 structure [RAS]","PMPR_IFTRANSPORT_0","PMPR_IFTRANSPORT_0 structure pointer [RAS]","_mpr_mpr_iftransport_0","mprapi/MPR_IFTRANSPORT_0","mprapi/PMPR_IFTRANSPORT_0","rras.mpr_iftransport_0"]
old-location: rras\mpr_iftransport_0.htm
tech.root: RRAS
ms.assetid: 4ee360be-fe5f-477e-901f-92d083f68451
ms.date: 12/05/2018
ms.keywords: '*PMPR_IFTRANSPORT_0, MPR_IFTRANSPORT_0, MPR_IFTRANSPORT_0 structure [RAS], PMPR_IFTRANSPORT_0, PMPR_IFTRANSPORT_0 structure pointer [RAS], _mpr_mpr_iftransport_0, mprapi/MPR_IFTRANSPORT_0, mprapi/PMPR_IFTRANSPORT_0, rras.mpr_iftransport_0'
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
req.typenames: MPR_IFTRANSPORT_0, *PMPR_IFTRANSPORT_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _MPR_IFTRANSPORT_0
 - mprapi/_MPR_IFTRANSPORT_0
 - PMPR_IFTRANSPORT_0
 - mprapi/PMPR_IFTRANSPORT_0
 - MPR_IFTRANSPORT_0
 - mprapi/MPR_IFTRANSPORT_0
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
 - MPR_IFTRANSPORT_0
---

# MPR_IFTRANSPORT_0 structure


## -description

The 
<b>MPR_IFTRANSPORT_0</b> structure contains information for a particular interface transport.

## -struct-fields

### -field dwTransportId

Identifies the transport.

### -field hIfTransport

Handle to the interface transport.

### -field wszIfTransportName

Specifies a Unicode string that contains the name of the interface transport.

## -see-also

<a href="/windows/desktop/api/mprapi/ns-mprapi-mpr_transport_0">MPR_TRANSPORT_0</a>



<a href="/windows/desktop/api/mprapi/nf-mprapi-mprconfiginterfacetransportenum">MprConfigInterfaceTransportEnum</a>



<a href="/windows/desktop/RRAS/router-management-reference">Router Management Reference</a>



<a href="/windows/desktop/RRAS/router-management-structures">Router Management Structures</a>