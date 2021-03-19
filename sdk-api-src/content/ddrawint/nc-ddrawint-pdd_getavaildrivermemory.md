---
UID: NC:ddrawint.PDD_GETAVAILDRIVERMEMORY
title: PDD_GETAVAILDRIVERMEMORY (ddrawint.h)
description: The DdGetAvailDriverMemory callback function queries the amount of free memory in the driver-managed memory heap.
helpviewer_keywords: ["DdGetAvailDriverMemory","DdGetAvailDriverMemory callback function [Display Devices]","PDD_GETAVAILDRIVERMEMORY","PDD_GETAVAILDRIVERMEMORY callback","ddfncs_670b3444-286c-4258-9936-9cb7995d0b24.xml","ddrawint/DdGetAvailDriverMemory","display.ddgetavaildrivermemory"]
old-location: display\ddgetavaildrivermemory.htm
tech.root: display
ms.assetid: 21a1988a-1bfd-47b8-b4b6-1bc137b2ba64
ms.date: 12/05/2018
ms.keywords: DdGetAvailDriverMemory, DdGetAvailDriverMemory callback function [Display Devices], PDD_GETAVAILDRIVERMEMORY, PDD_GETAVAILDRIVERMEMORY callback, ddfncs_670b3444-286c-4258-9936-9cb7995d0b24.xml, ddrawint/DdGetAvailDriverMemory, display.ddgetavaildrivermemory
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PDD_GETAVAILDRIVERMEMORY
 - ddrawint/PDD_GETAVAILDRIVERMEMORY
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdGetAvailDriverMemory
---



## -description

The <b>DdGetAvailDriverMemory</b> callback function queries the amount of free memory in the driver-managed memory heap.

## -parameters

### -param unnamedParam1


Points to a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getavaildrivermemorydata">DD_GETAVAILDRIVERMEMORYDATA</a> structure that contains the information required to perform the query.

## -returns

<b>DdGetAvailDriverMemory</b> returns one of the following callback codes:

## -remarks

This function does not need to be implemented if the memory will be managed by DirectDraw.

<b>DdGetAvailDriverMemory</b> determines how much free memory is in the driver's private heaps for the specified surface type. The driver should check the surface capabilities specified in the <b>DDSCaps</b> member of the following structure against the heaps it is maintaining internally, to determine what heap size to query. For example, if DDSCAPS_NONLOCALVIDMEM is set, the driver should return only contributions from the AGP heaps.

The driver indicates its support of <b>DdGetAvailDriverMemory</b> by implementing a response to GUID_MiscellaneousCallbacks in <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>.

## -see-also

<a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_getavaildrivermemorydata">DD_GETAVAILDRIVERMEMORYDATA</a>



<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>