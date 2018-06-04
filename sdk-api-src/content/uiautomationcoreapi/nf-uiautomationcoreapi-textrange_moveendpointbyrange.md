---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# TextRange_MoveEndpointByRange function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Moves an endpoint of one range to the endpoint of another range.


## -parameters




### -param hobj [in]

Type: <b>HUIATEXTRANGE</b>

The text range object whose endpoint is to move.


### -param endpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The endpoint to move (either the start or the end).


### -param targetRange [in]

Type: <b>HUIATEXTRANGE</b>

The text range that contains the target endpoint.


### -param targetEndpoint [in]

Type: <b>TextPatternRangeEndpoint</b>

The target endpoint to move to (either the start or the end).


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.



