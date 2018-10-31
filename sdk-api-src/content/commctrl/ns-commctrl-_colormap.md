---
UID: NS:commctrl._COLORMAP
title: "_COLORMAP"
author: windows-sdk-content
description: Contains information used by the CreateMappedBitmap function to map the colors of the bitmap.
old-location: controls\COLORMAP.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\toolbar\structures\colormap.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*LPCOLORMAP, COLORMAP, COLORMAP structure [Windows Controls], LPCOLORMAP, LPCOLORMAP structure pointer [Windows Controls], _COLORMAP, _win32_COLORMAP, _win32_COLORMAP_cpp, commctrl/COLORMAP, commctrl/LPCOLORMAP, controls.COLORMAP, controls._win32_COLORMAP"
ms.prod: windows
ms.technology: windows-sdk
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
---

# _COLORMAP structure


## -description


Contains information used by the <a href="https://msdn.microsoft.com/en-us/library/Bb787467(v=VS.85).aspx">CreateMappedBitmap</a> function to map the colors of the bitmap. 


## -struct-fields




### -field from

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">COLORREF</a></b>

Color to map from. 


### -field to

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Aa383751(v=VS.85).aspx">COLORREF</a></b>

Color to map to. 

