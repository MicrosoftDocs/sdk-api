---
UID: NS:ddrawint._DD_GETAVAILDRIVERMEMORYDATA
title: "_DD_GETAVAILDRIVERMEMORYDATA"
author: windows-driver-content
description: The DD_GETAVAILDRIVERMEMORYDATA structure contains the information needed by the driver to query and return the amount of free memory.
old-location: display\dd_getavaildrivermemorydata.htm
old-project: display
ms.assetid: 4e344c43-55ae-49fc-94ef-390c399d5d0b
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: "*PDD_GETAVAILDRIVERMEMORYDATA, DD_GETAVAILDRIVERMEMORYDATA, DD_GETAVAILDRIVERMEMORYDATA structure [Display Devices], _DD_GETAVAILDRIVERMEMORYDATA, ddrawint/DD_GETAVAILDRIVERMEMORYDATA, ddstrcts_874c0a25-9513-44fa-bbfc-a480c918a835.xml, display.dd_getavaildrivermemorydata"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: "*PDD_GETAVAILDRIVERMEMORYDATA, DD_GETAVAILDRIVERMEMORYDATA"
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	ddrawint.h
api_name:
-	DD_GETAVAILDRIVERMEMORYDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_GETAVAILDRIVERMEMORYDATA structure


## -description


The DD_GETAVAILDRIVERMEMORYDATA structure contains the information needed by the driver to query and return the amount of free memory.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550586">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field DDSCaps

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550286">DDSCAPS</a> structure that describes the type of surface for which memory availability is being queried.


### -field dwTotal

Specifies the location in which the driver returns the number of bytes of driver-managed memory that can be used for surfaces of the type described by <b>DDSCaps</b>.


### -field dwFree

Specifies the location in which the driver returns the amount of free memory in bytes for the surface type described by <b>DDSCaps</b>.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/21a1988a-1bfd-47b8-b4b6-1bc137b2ba64">DdGetAvailDriverMemory</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field GetAvailDriverMemory

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/21a1988a-1bfd-47b8-b4b6-1bc137b2ba64">DdGetAvailDriverMemory</a>
 

 

