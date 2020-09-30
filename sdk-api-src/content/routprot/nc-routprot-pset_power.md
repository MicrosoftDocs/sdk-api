---
UID: NC:routprot.PSET_POWER
title: PSET_POWER (routprot.h)
description: The SetPower function is reserved for future use.
helpviewer_keywords: ["PSET_POWER","PSET_POWER callback","SetPower","SetPower callback function [RAS]","_mpr_setpower","routprot/SetPower","rras.setpower"]
old-location: rras\setpower.htm
tech.root: RRAS
ms.assetid: 595e1743-04eb-4490-8548-1ce5ce00e144
ms.date: 12/05/2018
ms.keywords: PSET_POWER, PSET_POWER callback, SetPower, SetPower callback function [RAS], _mpr_setpower, routprot/SetPower, rras.setpower
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
 - PSET_POWER
 - routprot/PSET_POWER
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
 - SetPower
---

# PSET_POWER callback function


## -description

The 
<b>SetPower</b> function is reserved for future use. It is not currently called by the router manager. Routing protocols should pass <b>NULL</b> as the pointer value for this function in 
<a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">MPR_ROUTING_CHARACTERISTICS</a>


The <a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">PSET_POWER</a> type defines a pointer to this callback function. <i>SetPower</i> is a placeholder for the application-defined function name.

## -parameters

### -param PowerType [in]

Reserved for future use.

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pquery_power">QueryPower</a>