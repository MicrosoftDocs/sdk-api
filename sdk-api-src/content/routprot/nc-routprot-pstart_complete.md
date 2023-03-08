---
UID: NC:routprot.PSTART_COMPLETE
title: PSTART_COMPLETE (routprot.h)
description: Router Manager calls the StartComplete function to inform the routing protocol that initialization is complete and all interfaces have been added. The routing protocol should wait for this call before starting any protocol-specific behavior.
helpviewer_keywords: ["PSTART_COMPLETE","PSTART_COMPLETE callback","StartComplete","StartComplete callback function [RAS]","_mpr_startcomplete","routprot/StartComplete","rras.startcomplete"]
old-location: rras\startcomplete.htm
tech.root: RRAS
ms.assetid: 1dace3a7-8e97-405c-b1fe-f5a67c05fb0c
ms.date: 12/05/2018
ms.keywords: PSTART_COMPLETE, PSTART_COMPLETE callback, StartComplete, StartComplete callback function [RAS], _mpr_startcomplete, routprot/StartComplete, rras.startcomplete
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
 - PSTART_COMPLETE
 - routprot/PSTART_COMPLETE
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
 - StartComplete
---

# PSTART_COMPLETE callback function


## -description

Router Manager calls the 
<b>StartComplete</b> function to inform the routing protocol that initialization is complete and all interfaces have been added. The routing protocol should wait for this call before starting any protocol-specific behavior.

The <a href="/windows/desktop/api/routprot/ns-routprot-mpr50_routing_characteristics">PSTART_COMPLETE</a> type defines a pointer to this callback function. <i>StartComplete</i> is a placeholder for the application-defined function name.

## -parameters

### -param unnamedParam1

## -returns

This function should return NO_ERROR.

## -see-also

<a href="/windows/desktop/api/routprot/nc-routprot-pstart_protocol">StartProtocol</a>