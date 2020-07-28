---
UID: NF:rtmv2.RTM_SIZE_OF_ROUTE_INFO
title: RTM_SIZE_OF_ROUTE_INFO macro (rtmv2.h)
description: The RTM_SIZE_OF_ROUTE_INFO macro returns the size of the route information structure, RTM_ROUTE_INFO.
helpviewer_keywords: ["RTM_SIZE_OF_ROUTE_INFO","RTM_SIZE_OF_ROUTE_INFO macro [RAS]","_rtmv2ref_rtm_size_of_route_info","rras.rtm_size_of_route_info","rtmv2/RTM_SIZE_OF_ROUTE_INFO"]
old-location: rras\rtm_size_of_route_info.htm
tech.root: RRAS
ms.assetid: ef3308a1-9a5e-4162-91d1-6ae2abff5c3b
ms.date: 12/05/2018
ms.keywords: RTM_SIZE_OF_ROUTE_INFO, RTM_SIZE_OF_ROUTE_INFO macro [RAS], _rtmv2ref_rtm_size_of_route_info, rras.rtm_size_of_route_info, rtmv2/RTM_SIZE_OF_ROUTE_INFO
f1_keywords:
- rtmv2/RTM_SIZE_OF_ROUTE_INFO
dev_langs:
- c++
req.header: rtmv2.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Rtmv2.h
api_name:
- RTM_SIZE_OF_ROUTE_INFO
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RTM_SIZE_OF_ROUTE_INFO macro


## -description


The 
<b>RTM_SIZE_OF_ROUTE_INFO</b> macro returns the size of the route information structure, 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a>. The size of this structure is variable, and is based on the number of next hops associated with the route. Use this macro when allocating memory for route structures.


## -parameters




### -param NumHops

Specifies the number of next hops in the route structure.


## -remarks



If the client  only allocates one next hop per route, the client can allocate an 
<a href="https://docs.microsoft.com/windows/desktop/api/rtmv2/ns-rtmv2-rtm_route_info">RTM_ROUTE_INFO</a> structure statically.

The macro is defined as follows:


```cpp
#include <windows.h>

#define RTM_SIZE_OF_ROUTE_INFO(NumHops)                     \
    FIELD_OFFSET(RTM_ROUTE_INFO, NextHopsList.NumNextHops)

#define RTM_BASIC_ROUTE_INFO_SIZE                           \
    (RTM_BASIC_ROUTE_INFO_SIZE + (NumHops) *                \
     sizeof(RTM_NEXTHOP_HANDLE))

```




