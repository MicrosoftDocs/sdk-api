---
UID: NS:ddrawint._DD_GETAVAILDRIVERMEMORYDATA
title: DD_GETAVAILDRIVERMEMORYDATA (ddrawint.h)
description: The DD_GETAVAILDRIVERMEMORYDATA structure contains the information needed by the driver to query and return the amount of free memory.
helpviewer_keywords: ["*PDD_GETAVAILDRIVERMEMORYDATA","DD_GETAVAILDRIVERMEMORYDATA","DD_GETAVAILDRIVERMEMORYDATA structure [Display Devices]","ddrawint/DD_GETAVAILDRIVERMEMORYDATA","ddstrcts_874c0a25-9513-44fa-bbfc-a480c918a835.xml","display.dd_getavaildrivermemorydata"]
old-location: display\dd_getavaildrivermemorydata.htm
tech.root: display
ms.assetid: 4e344c43-55ae-49fc-94ef-390c399d5d0b
ms.date: 12/05/2018
ms.keywords: '*PDD_GETAVAILDRIVERMEMORYDATA, DD_GETAVAILDRIVERMEMORYDATA, DD_GETAVAILDRIVERMEMORYDATA structure [Display Devices], ddrawint/DD_GETAVAILDRIVERMEMORYDATA, ddstrcts_874c0a25-9513-44fa-bbfc-a480c918a835.xml, display.dd_getavaildrivermemorydata'
req.header: ddrawint.h
req.include-header: Winddi.h
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
targetos: Windows
req.typenames: '*PDD_GETAVAILDRIVERMEMORYDATA, DD_GETAVAILDRIVERMEMORYDATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETAVAILDRIVERMEMORYDATA
 - ddrawint/_DD_GETAVAILDRIVERMEMORYDATA
 - PDD_GETAVAILDRIVERMEMORYDATA
 - ddrawint/PDD_GETAVAILDRIVERMEMORYDATA
 - DD_GETAVAILDRIVERMEMORYDATA
 - ddrawint/DD_GETAVAILDRIVERMEMORYDATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_GETAVAILDRIVERMEMORYDATA
---

# DD_GETAVAILDRIVERMEMORYDATA structure


## -description

The DD_GETAVAILDRIVERMEMORYDATA structure contains the information needed by the driver to query and return the amount of free memory.

## -struct-fields

### -field lpDD

Points to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_directdraw_global">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.

### -field DDSCaps

Points to a <a href="/previous-versions/windows/hardware/drivers/ff550286(v=vs.85)">DDSCAPS</a> structure that describes the type of surface for which memory availability is being queried.

### -field dwTotal

Specifies the location in which the driver returns the number of bytes of driver-managed memory that can be used for surfaces of the type described by <b>DDSCaps</b>.

### -field dwFree

Specifies the location in which the driver returns the amount of free memory in bytes for the surface type described by <b>DDSCaps</b>.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getavaildrivermemory">DdGetAvailDriverMemory</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

### -field GetAvailDriverMemory

Used by the Microsoft DirectDraw API and should not be filled in by the driver.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getavaildrivermemory">DdGetAvailDriverMemory</a>