---
UID: NF:winddi.DrvSaveScreenBits
title: DrvSaveScreenBits function
author: windows-sdk-content
description: The DrvSaveScreenBits function causes a display driver to save or restore a given rectangle of the displayed image.
old-location: display\drvsavescreenbits.htm
tech.root: display
ms.assetid: c91c860f-502e-4bd6-9a0b-653e5ef14735
ms.author: windowssdkdev
ms.date: 08/13/2018
ms.keywords: DrvSaveScreenBits, DrvSaveScreenBits function [Display Devices], ddifncs_36f63073-3525-4300-941f-709aba9204c7.xml, display.drvsavescreenbits, winddi/DrvSaveScreenBits
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winddi.h
api_name:
 - DrvSaveScreenBits
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvSaveScreenBits function


## -description


The <b>DrvSaveScreenBits</b> function causes a display driver to save or restore a given rectangle of the displayed image.


## -parameters




### -param pso

Pointer to a <a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a> structure that describes the surface.


### -param iMode

Specifies the operation to perform. This parameter can be one of the following values:





#### SS_SAVE

The driver should save the data from the rectangle defined by <i>prcl</i>. The driver is responsible for managing this data in its <a href="https://msdn.microsoft.com/3f78ce93-03cd-45aa-9861-cdf6d557e6a5">off-screen memory</a>. The <i>ident</i> parameter is ignored.

Upon success, <b>DrvSaveScreenBits</b> should return an identifier for the saved data. The driver can return a handle or even a pointer to its off-screen memory. This function returns zero if it fails.



#### SS_RESTORE

The driver should restore the data identified by <i>ident</i> to the rectangle <i>prcl</i> on the display; that is, the driver should restore the bitmap to its original position. The driver can assume that the rectangle at <i>prcl</i> is exactly the same size as the rectangle that was saved. The data should be discarded after this call.

<b>DrvSaveScreenBits</b> should return <b>TRUE</b> if the data has been restored to the display, or <b>FALSE</b> if the data cannot be restored.



#### SS_FREE

The data identified by <i>ident</i> is no longer needed and can be freed. The value of <i>prcl</i> is undefined and should not be used. The driver should not restore the saved rectangle to the display.

<b>DrvSaveScreenBits</b> should return <b>TRUE</b>.


### -param ident

Pointer to a driver-defined value  that was returned by a previous call to <b>DrvSaveScreenBits</b> if <i>iMode</i> is SS_RESTORE or SS_FREE. The driver should ignore this parameter when <i>iMode</i> is SS_SAVE.


### -param prcl

Pointer to a <a href="https://msdn.microsoft.com/709f8262-829e-4cda-bb0b-564307edfd24">RECTL</a> structure that defines the portion of the screen to be saved or restored.


## -returns



The return value is dependent on the value of the <i>iMode</i> parameter.




## -remarks



Some display drivers might be able to move data to or from off-screen device memory much faster than the area can be redrawn. This might be useful when Window Manager must display a menu or dialog box.

<b>DrvSaveScreenBits</b> is optional for display drivers.




## -see-also




<a href="https://msdn.microsoft.com/cee7cb50-1e8a-422b-aebe-7030ae96fb34">SURFOBJ</a>
 

 

