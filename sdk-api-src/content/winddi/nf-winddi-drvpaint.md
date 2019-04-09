---
UID: NF:winddi.DrvPaint
title: DrvPaint function (winddi.h)
author: windows-sdk-content
description: The DrvPaint function is obsolete, and is no longer called by GDI in Windows 2000 and later. New drivers should implement one or more of DrvFillPath, DrvStrokePath, or DrvStrokeAndFillPath.
old-location: display\drvpaint.htm
tech.root: display
ms.assetid: c4e3fa2c-44f9-4160-8d0b-3021ad18a472
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DrvPaint, DrvPaint function [Display Devices], ddifncs_34ade16d-3f7c-42b3-a020-388ec6a36f27.xml, display.drvpaint, winddi/DrvPaint
ms.topic: function
req.header: winddi.h
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
 - winddi.h
api_name:
 - DrvPaint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrvPaint function


## -description


The <b>DrvPaint</b> function is obsolete, and is no longer called by GDI in Windows 2000 and later. New drivers should implement one or more of <a href="https://msdn.microsoft.com/6f499d08-d2a1-46d0-b931-e6c16c4e1d3a">DrvFillPath</a>, <a href="https://msdn.microsoft.com/c931a39d-c0ae-4f40-b70f-f51d5621c228">DrvStrokePath</a>, or <a href="https://msdn.microsoft.com/92a04fe5-146d-4839-a854-1ac50705b447">DrvStrokeAndFillPath</a>.


## -parameters




### -param pso [in]


### -param pco [in]


### -param pbo [in]


### -param pptlBrushOrg [in]


### -param mix [in]

