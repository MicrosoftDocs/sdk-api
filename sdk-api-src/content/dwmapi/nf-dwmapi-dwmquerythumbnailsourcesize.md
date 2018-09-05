---
UID: NF:dwmapi.DwmQueryThumbnailSourceSize
title: DwmQueryThumbnailSourceSize function
author: windows-sdk-content
description: Retrieves the source size of the Desktop Window Manager (DWM) thumbnail.
old-location: dwm\dwmquerythumbnailsourcesize.htm
old-project: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmquerythumbnailsourcesize.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DwmQueryThumbnailSourceSize, DwmQueryThumbnailSourceSize function [Desktop Window Manager], _udwm_dwmquerythumbnailsourcesize, _udwm_dwmquerythumbnailsourcesize_cpp, dwm.dwmquerythumbnailsourcesize, dwmapi/DwmQueryThumbnailSourceSize, winui._udwm_dwmquerythumbnailsourcesize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dwmapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
api_name:
 - DwmQueryThumbnailSourceSize
product: Windows
targetos: Windows
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DwmQueryThumbnailSourceSize function


## -description


Retrieves the source size of the Desktop Window Manager (DWM) thumbnail.


## -parameters




### -param hThumbnail

A handle to the thumbnail to retrieve the source window size from.


### -param pSize [out]

A pointer to a <a href="https://msdn.microsoft.com/8cb0802c-1868-4f3b-8287-c6fb1fa7ab68">SIZE</a> structure that, when this function returns successfully, receives the size of the source thumbnail.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/6d71fcda-0cf0-463c-8c60-0415109d154f">DWM Thumbnail Overview</a>



<a href="https://msdn.microsoft.com/fb1e0f1e-a6db-4961-bfa5-9c2218f8c950">Desktop Window Manager Overview</a>



<a href="https://msdn.microsoft.com/02c40cda-b87c-44c5-bcc5-3d0e83b7b14b">DwmUpdateThumbnailProperties</a>
 

 

