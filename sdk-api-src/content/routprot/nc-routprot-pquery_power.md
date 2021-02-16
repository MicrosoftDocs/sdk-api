---
UID: NC:routprot.PQUERY_POWER
title: PQUERY_POWER (routprot.h)
description: The QueryPower function is reserved for future use.
helpviewer_keywords: ["PQUERY_POWER","PQUERY_POWER callback","QueryPower","QueryPower callback function [RAS]","_mpr_querypower","routprot/QueryPower","rras.querypower"]
old-location: rras\querypower.htm
tech.root: RRAS
ms.assetid: 591082fb-ef1e-4271-bf6c-d5034bdbae99
ms.date: 12/05/2018
ms.keywords: PQUERY_POWER, PQUERY_POWER callback, QueryPower, QueryPower callback function [RAS], _mpr_querypower, routprot/QueryPower, rras.querypower
req.header: routprot.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PQUERY_POWER
 - routprot/PQUERY_POWER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - QueryPower
---

# PQUERY_POWER callback function


## -description

The 
<i>QueryPower</i> function is reserved for future use. It is not currently called by the router manager. Routing protocols should pass <b>NULL</b> as the pointer value for this function in 
<a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">MPR_ROUTING_CHARACTERISTICS</a>


The <a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">PQUERY_POWER</a> type defines a pointer to this callback function. <i>QueryPower</i> is a placeholder for the application-defined function name.

## -parameters

### -param PowerType [in]

Reserved for future use.

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pset_power">SetPower</a>