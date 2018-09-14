---
UID: NF:winddi.XLATEOBJ_piVector
title: XLATEOBJ_piVector function
author: windows-sdk-content
description: The XLATEOBJ_piVector function retrieves a translation vector that the driver can use to translate source indices to destination indices.
old-location: display\xlateobj_pivector.htm
tech.root: display
ms.assetid: 7dcfd280-26af-47ff-a5a6-50325e6471bc
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: XLATEOBJ_piVector, XLATEOBJ_piVector function [Display Devices], display.xlateobj_pivector, gdifncs_875168b9-8752-46cb-9198-53af5769db5b.xml, winddi/XLATEOBJ_piVector
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winddi.h
req.include-header: Winddi.h
req.target-type: Universal
req.target-min-winverclnt: Available in Windows 2000 and later versions of the Windows operating systems.
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
req.lib: Win32k.lib
req.dll: Win32k.sys
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Win32k.sys
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - XLATEOBJ_piVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# XLATEOBJ_piVector function


## -description


The <b>XLATEOBJ_piVector</b> function retrieves a translation vector that the driver can use to translate source indices to destination indices.


## -parameters




### -param pxlo

Pointer to a <a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a> structure that defines the indexed source object.


## -returns



The return value is a pointer to a vector of translation entries if the function is successful. Otherwise, it is null, and an error code is logged.




## -remarks



This function can be used only if the source palette is an indexed palette.




## -see-also




<a href="https://msdn.microsoft.com/08bdead0-290a-4b23-8118-5f1f941e439f">XLATEOBJ</a>
 

 

