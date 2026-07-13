---
UID: NF:winddi.EngDeleteSurface
title: EngDeleteSurface function (winddi.h)
description: The EngDeleteSurface function deletes the specified surface.
helpviewer_keywords: ["EngDeleteSurface","EngDeleteSurface function [Display Devices]","display.engdeletesurface","gdifncs_7ffbac74-6789-4f81-a4eb-4f6f1c41a444.xml","winddi/EngDeleteSurface"]
old-location: display\engdeletesurface.htm
tech.root: display
ms.assetid: 9cde6fa3-26b6-49fd-9374-cbf91215aa39
ms.date: 12/05/2018
ms.keywords: EngDeleteSurface, EngDeleteSurface function [Display Devices], display.engdeletesurface, gdifncs_7ffbac74-6789-4f81-a4eb-4f6f1c41a444.xml, winddi/EngDeleteSurface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EngDeleteSurface
 - winddi/EngDeleteSurface
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-core-win32k-base-export-l1-1-0.dll
 - Win32k.sys
api_name:
 - EngDeleteSurface
---

# EngDeleteSurface function


## -description

The <b>EngDeleteSurface</b> function deletes the specified surface.

## -parameters

### -param hsurf [in]

Handle to the surface to delete. This handle can be an HSURF or HBM.

## -returns

<b>EngDeleteSurface</b> returns <b>TRUE</b> if it is successful in deleting the surface. Otherwise, it returns <b>FALSE</b> and an error code is logged.

