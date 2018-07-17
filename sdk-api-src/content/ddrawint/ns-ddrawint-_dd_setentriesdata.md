---
UID: NS:ddrawint._DD_SETENTRIESDATA
title: "_DD_SETENTRIESDATA"
author: windows-sdk-content
description: The DD_SETENTRIESDATA structure contains information necessary to set palette entries.
old-location: display\dd_setentriesdata.htm
old-project: display
ms.assetid: 9420f41a-401b-4fc3-b9a4-f2bfe6cb2710
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: "*PDD_SETENTRIESDATA, DD_SETENTRIESDATA, DD_SETENTRIESDATA structure [Display Devices], _DD_SETENTRIESDATA, ddrawint/DD_SETENTRIESDATA, ddstrcts_dc575bf2-1249-4d66-aba9-aba1856358df.xml, display.dd_setentriesdata"
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
req.typenames: "*PDD_SETENTRIESDATA, DD_SETENTRIESDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_SETENTRIESDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_SETENTRIESDATA structure


## -description


The DD_SETENTRIESDATA structure contains information necessary to set palette entries.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550586">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDPalette

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551684">DD_PALETTE_GLOBAL</a> structure that represents the DirectDrawPalette object.


### -field dwBase

Specifies a zero-based index into the color table of the first entry to be modified.


### -field dwNumEntries

Specifies the number of palette entries that the driver should update.


### -field lpEntries

Points to a PALETTEENTRY structure that specifies the color table. See the latest Microsoft DirectX SDK documentation for more information about PALETTEENTRY.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/41b0b433-288d-4d7b-b961-2789b2540761">DdSetEntries</a> callback. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field SetEntries

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/41b0b433-288d-4d7b-b961-2789b2540761">DdSetEntries</a>
 

 

