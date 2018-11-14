---
UID: NS:ddrawint._DD_GETSCANLINEDATA
title: "_DD_GETSCANLINEDATA"
author: windows-sdk-content
description: The DD_GETSCANLINEDATA structure contains the members required to query and return the number of the current scan line.
old-location: display\dd_getscanlinedata.htm
tech.root: display
ms.assetid: 92433daa-43da-40d3-a319-e0d70abd3cb0
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PDD_GETSCANLINEDATA, DD_GETSCANLINEDATA, DD_GETSCANLINEDATA structure [Display Devices], _DD_GETSCANLINEDATA, ddrawint/DD_GETSCANLINEDATA, ddstrcts_f7654548-917a-4c6d-a15a-0f09bca64b5d.xml, display.dd_getscanlinedata"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_GETSCANLINEDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_GETSCANLINEDATA, DD_GETSCANLINEDATA"
req.redist: 
---

# _DD_GETSCANLINEDATA structure


## -description


The DD_GETSCANLINEDATA structure contains the members required to query and return the number of the current scan line.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field dwScanLine

Specifies the location in which the driver returns the number of the current scan line. See the Remarks section for more information.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/3738205f-2d27-4211-944a-6ca71954fe47">DdGetScanLine</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field GetScanLine

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


## -remarks



The returned scan line value in <b>dwScanLine</b> must be greater than or equal to 0 and less than N, where N is the sum of the number of visible scan lines and the number of scan lines that occur during vertical blank. For example, with a display operating at a resolution of 640x480, that has 12 scan lines during vertical blank, the value returned to <b>GetScanLine</b> could range from 0 to 491.




## -see-also




<a href="https://msdn.microsoft.com/3738205f-2d27-4211-944a-6ca71954fe47">DdGetScanLine</a>
 

 

