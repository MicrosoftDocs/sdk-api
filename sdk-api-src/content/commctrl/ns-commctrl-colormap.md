---
UID: NS:commctrl._COLORMAP
title: COLORMAP (commctrl.h)
author: windows-sdk-content
description: Contains information used by the CreateMappedBitmap function to map the colors of the bitmap.
old-location: controls\COLORMAP.htm
tech.root: Controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\colormap.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*LPCOLORMAP, COLORMAP, COLORMAP structure [Windows Controls], LPCOLORMAP, LPCOLORMAP structure pointer [Windows Controls], _win32_COLORMAP, _win32_COLORMAP_cpp, commctrl/COLORMAP, commctrl/LPCOLORMAP, controls.COLORMAP, controls._win32_COLORMAP"
ms.topic: struct
req.header: commctrl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - Commctrl.h
api_name:
 - COLORMAP
product: Windows
targetos: Windows
req.typenames: COLORMAP, *LPCOLORMAP
req.redist: 
ms.custom: 19H1
---

# COLORMAP structure


## -description


Contains information used by the <a href="https://docs.microsoft.com/windows/desktop/api/commctrl/nf-commctrl-createmappedbitmap">CreateMappedBitmap</a> function to map the colors of the bitmap. 


## -struct-fields




### -field from

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Color to map from. 


### -field to

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">COLORREF</a></b>

Color to map to. 

