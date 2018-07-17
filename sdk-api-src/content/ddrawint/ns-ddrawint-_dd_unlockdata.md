---
UID: NS:ddrawint._DD_UNLOCKDATA
title: "_DD_UNLOCKDATA"
author: windows-sdk-content
description: The DD_UNLOCKDATA structure contains information necessary to do an unlock as defined by Microsoft DirectDraw parameter structures.
old-location: display\dd_unlockdata.htm
old-project: display
ms.assetid: 4642f596-376f-4f63-bf6e-916112ce1ec9
ms.author: windowssdkdev
ms.date: 07/12/2018
ms.keywords: "*PDD_UNLOCKDATA, DD_UNLOCKDATA, DD_UNLOCKDATA structure [Display Devices], _DD_UNLOCKDATA, ddrawint/DD_UNLOCKDATA, ddstrcts_1784fe3c-5a41-4428-ac94-06226857ae9a.xml, display.dd_unlockdata"
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
req.typenames: "*PDD_UNLOCKDATA, DD_UNLOCKDATA"
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_UNLOCKDATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _DD_UNLOCKDATA structure


## -description


The DD_UNLOCKDATA structure contains information necessary to do an unlock as defined by Microsoft DirectDraw parameter structures.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550586">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDSurface

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551733">DD_SURFACE_LOCAL</a> structure that describes the surface--in the case of <a href="https://msdn.microsoft.com/ab0476f5-64da-415e-a8aa-ccbfc9f1a082">UnlockD3DBuffer</a>, a buffer--to be unlocked.


### -field ddRVal

Specifies the location in which the driver writes the return value of either the <a href="https://msdn.microsoft.com/dbb7b34c-5473-42b9-b16f-e71b9c3e1db8">DdUnlock</a> or <a href="https://msdn.microsoft.com/ab0476f5-64da-415e-a8aa-ccbfc9f1a082">UnlockD3DBuffer</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field Unlock

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/dbb7b34c-5473-42b9-b16f-e71b9c3e1db8">DdUnlock</a>



<a href="https://msdn.microsoft.com/ab0476f5-64da-415e-a8aa-ccbfc9f1a082">UnlockD3DBuffer</a>
 

 

