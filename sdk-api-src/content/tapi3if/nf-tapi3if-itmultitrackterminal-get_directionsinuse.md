---
UID: NF:tapi3if.ITMultiTrackTerminal.get_DirectionsInUse
title: ITMultiTrackTerminal::get_DirectionsInUse
author: windows-sdk-content
description: The get_DirectionsInUse method returns the direction of all tracks managed currently by the multitrack terminal.
old-location: tapi3\itmultitrackterminal_get_directionsinuse.htm
tech.root: tapi
ms.assetid: d9f739ea-3df5-4275-868a-3e0d611254c0
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITMultiTrackTerminal interface [TAPI 2.2],get_DirectionsInUse method, ITMultiTrackTerminal.get_DirectionsInUse, ITMultiTrackTerminal::get_DirectionsInUse, _tapi3_itmultitrackterminal_get_directionsinuse, get_DirectionsInUse, get_DirectionsInUse method [TAPI 2.2], get_DirectionsInUse method [TAPI 2.2],ITMultiTrackTerminal interface, tapi3.itmultitrackterminal_get_directionsinuse, tapi3if/ITMultiTrackTerminal::get_DirectionsInUse
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMultiTrackTerminal.get_DirectionsInUse
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITMultiTrackTerminal::get_DirectionsInUse


## -description


The 
<b>get_DirectionsInUse</b> method returns the direction of all tracks managed currently by the multitrack terminal. For tracks that are multitrack terminals themselves, this method calls the track's <b>ITMultiTrackTerminal::get_DirectionsInUse</b> method to determine the track's directions.


## -parameters




### -param plDirectionsInUsed [out]

Pointer to the 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">TERMINAL_DIRECTION</a> descriptor of the directions.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c9e5d8a4-78a6-4449-9c11-c780e72ab925">ITMultiTrackTerminal</a>
 

 

