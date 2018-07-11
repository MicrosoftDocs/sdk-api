---
UID: NS:ddrawint._DD_SETEXCLUSIVEMODEDATA
title: "_DD_SETEXCLUSIVEMODEDATA"
author: windows-sdk-content
description: The DD_SETEXCLUSIVEMODEDATA structure contains the exclusive mode notification information.
old-location: display\dd_setexclusivemodedata.htm
old-project: display
ms.assetid: b2f5af15-c773-4741-a8dc-71d2b89776a7
ms.author: windowssdkdev
ms.date: 06/26/2018
ms.keywords: "*PDD_SETEXCLUSIVEMODEDATA, DD_SETEXCLUSIVEMODEDATA, DD_SETEXCLUSIVEMODEDATA structure [Display Devices], _DD_SETEXCLUSIVEMODEDATA, ddrawint/DD_SETEXCLUSIVEMODEDATA, ddstrcts_c6ba3e13-afcd-4e8a-994b-d3c006d2c952.xml, display.dd_setexclusivemodedata"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: "*PDD_SETEXCLUSIVEMODEDATA, DD_SETEXCLUSIVEMODEDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_SETEXCLUSIVEMODEDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_SETEXCLUSIVEMODEDATA structure


## -description


The DD_SETEXCLUSIVEMODEDATA structure contains the exclusive mode notification information.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550586">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field dwEnterExcl

Indicates that a Microsoft DirectDraw application is switching into exclusive mode when <b>TRUE</b>; indicates that a DirectDraw application is leaving exclusive mode when <b>FALSE</b>.


### -field dwReserved

This is reserved for system use and should be ignored by the driver.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/c322a4ac-0900-4f31-9e02-923afdad5fd6">DdSetExclusiveMode</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field SetExclusiveMode

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/c322a4ac-0900-4f31-9e02-923afdad5fd6">DdSetExclusiveMode</a>
 

 

