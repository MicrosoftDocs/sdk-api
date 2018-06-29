---
UID: NF:dwmapi.DwmUnregisterThumbnail
title: DwmUnregisterThumbnail function
author: windows-sdk-content
description: Removes a Desktop Window Manager (DWM) thumbnail relationship created by the DwmRegisterThumbnail function.
old-location: dwm\dwmunregisterthumbnail.htm
old-project: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmunregisterthumbnail.htm
ms.author: windowssdkdev
ms.date: 03/14/2018
ms.keywords: DwmUnregisterThumbnail, DwmUnregisterThumbnail function [Desktop Window Manager], _udwm_dwmunregisterthumbnail, _udwm_dwmunregisterthumbnail_cpp, dwm.dwmunregisterthumbnail, dwmapi/DwmUnregisterThumbnail, winui._udwm_dwmunregisterthumbnail
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
 - DwmUnregisterThumbnail
product: Windows
targetos: Windows
req.lib: Dwmapi.lib
req.dll: Dwmapi.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DwmUnregisterThumbnail function


## -description


Removes a Desktop Window Manager (DWM) thumbnail relationship created by the <a href="https://msdn.microsoft.com/library/Aa969521(v=VS.85).aspx">DwmRegisterThumbnail</a> function.


## -parameters




### -param hThumbnailId

The handle to the thumbnail relationship to be removed. Null or non-existent handles will result in a return value of E_INVALIDARG.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Unregistering DWM thumbnail relationships must be done within the process that registered the relationships.




## -see-also




<a href="https://msdn.microsoft.com/library/Aa969541(v=VS.85).aspx">DWM Thumbnail Overview</a>



<a href="https://msdn.microsoft.com/library/Aa969540(v=VS.85).aspx">Desktop Window Manager Overview</a>



<a href="https://msdn.microsoft.com/library/Aa969520(v=VS.85).aspx">DwmQueryThumbnailSourceSize</a>



<a href="https://msdn.microsoft.com/library/Aa969526(v=VS.85).aspx">DwmUpdateThumbnailProperties</a>
 

 

