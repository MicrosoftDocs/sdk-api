---
UID: NE:strmif._FilterState
title: "_FilterState"
author: windows-sdk-content
description: Specifies a filter's state or the state of the filter graph.
old-location: dshow\filter_state.htm
tech.root: DirectShow
ms.assetid: 41f88abc-57d1-4f80-a099-d17e624ab8a6
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: FILTER_STATE, FILTER_STATE , FILTER_STATE enumeration [DirectShow], FILTER_STATEEnumeration, State_Paused, State_Running, State_Stopped, _FilterState, dshow.filter_state, strmif/FILTER_STATE, strmif/State_Paused, strmif/State_Running, strmif/State_Stopped
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - FILTER_STATE
product: Windows
targetos: Windows
req.typenames: FILTER_STATE
req.redist: 
---

# _FilterState enumeration


## -description



Specifies a filter's state or the state of the filter graph.




## -enum-fields




### -field State_Stopped

Stopped. The filter is not processing data.


### -field State_Paused

Paused. The filter is processing data, but not rendering it.


### -field State_Running

Running. The filter is processing and rendering data.


## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/653a94ff-6929-41b1-9b94-dccaff0f7ec7">IMediaControl::GetState</a>



<a href="https://msdn.microsoft.com/b20ca3e9-bec2-4c6d-ba80-f4dae2f5a831">IMediaFilter::GetState</a>
 

 

