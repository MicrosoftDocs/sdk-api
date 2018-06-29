---
UID: NC:routprot.PQUERY_POWER
title: PQUERY_POWER
author: windows-sdk-content
description: The QueryPower function is reserved for future use.
old-location: rras\querypower.htm
old-project: RRAS
ms.assetid: 591082fb-ef1e-4271-bf6c-d5034bdbae99
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: PQUERY_POWER, PQUERY_POWER callback, QueryPower, QueryPower callback function [RAS], _mpr_querypower, routprot/QueryPower, rras.querypower
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Routprot.h
api_name:
 - QueryPower
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# PQUERY_POWER callback function


## -description


The 
<i>QueryPower</i> function is reserved for future use. It is not currently called by the router manager. Routing protocols should pass <b>NULL</b> as the pointer value for this function in 
<a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">MPR_ROUTING_CHARACTERISTICS</a>


The <a href="https://msdn.microsoft.com/7046c4c2-b0bd-4459-b361-e46ce876823f">PQUERY_POWER</a> type defines a pointer to this callback function. <i>QueryPower</i> is a placeholder for the application-defined function name.


## -parameters




### -param PowerType [in]

Reserved for future use.


## -see-also




<a href="https://msdn.microsoft.com/595e1743-04eb-4490-8548-1ce5ce00e144">SetPower</a>
 

 

