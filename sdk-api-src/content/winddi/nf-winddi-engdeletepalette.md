---
UID: NF:winddi.EngDeletePalette
title: EngDeletePalette function
author: windows-sdk-content
description: The EngDeletePalette function sends a request to GDI to delete the specified palette.
old-location: display\engdeletepalette.htm
tech.root: display
ms.assetid: ebdbbb4e-aaa8-4fb7-9546-545dce803054
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: EngDeletePalette, EngDeletePalette function [Display Devices], display.engdeletepalette, gdifncs_221095fd-b5c5-485e-9e8c-9f7a114d496d.xml, winddi/EngDeletePalette
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
api_name:
 - EngDeletePalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EngDeletePalette function


## -description


The <b>EngDeletePalette</b> function sends a request to GDI to delete the specified palette.


## -parameters




### -param hpal [in]

Handle to the palette to be deleted. This handle is supplied by <a href="https://msdn.microsoft.com/99b27e11-5a5f-4fa7-9cd0-422d24425fa1">EngCreatePalette</a>.


## -returns



The return value is <b>TRUE</b> if the function is successful; otherwise, it returns <b>FALSE</b>.



