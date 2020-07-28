---
UID: NF:dwmapi.DwmQueryThumbnailSourceSize
title: DwmQueryThumbnailSourceSize function (dwmapi.h)
description: Retrieves the source size of the Desktop Window Manager (DWM) thumbnail.
helpviewer_keywords: ["DwmQueryThumbnailSourceSize","DwmQueryThumbnailSourceSize function [Desktop Window Manager]","_udwm_dwmquerythumbnailsourcesize","_udwm_dwmquerythumbnailsourcesize_cpp","dwm.dwmquerythumbnailsourcesize","dwmapi/DwmQueryThumbnailSourceSize","winui._udwm_dwmquerythumbnailsourcesize"]
old-location: dwm\dwmquerythumbnailsourcesize.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmquerythumbnailsourcesize.htm
ms.date: 12/05/2018
ms.keywords: DwmQueryThumbnailSourceSize, DwmQueryThumbnailSourceSize function [Desktop Window Manager], _udwm_dwmquerythumbnailsourcesize, _udwm_dwmquerythumbnailsourcesize_cpp, dwm.dwmquerythumbnailsourcesize, dwmapi/DwmQueryThumbnailSourceSize, winui._udwm_dwmquerythumbnailsourcesize
f1_keywords:
- dwmapi/DwmQueryThumbnailSourceSize
dev_langs:
- c++
req.header: dwmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmQueryThumbnailSourceSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DwmQueryThumbnailSourceSize function


## -description


Retrieves the source size of the Desktop Window Manager (DWM) thumbnail.


## -parameters




### -param hThumbnail

A handle to the thumbnail to retrieve the source window size from.


### -param pSize [out]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/dd145106(v=vs.85)">SIZE</a> structure that, when this function returns successfully, receives the size of the source thumbnail.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dwm/thumbnail-ovw">DWM Thumbnail Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/dwm/dwm-overview">Desktop Window Manager Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dwmapi/nf-dwmapi-dwmupdatethumbnailproperties">DwmUpdateThumbnailProperties</a>
 

 

