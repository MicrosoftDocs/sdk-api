---
UID: NF:dwmapi.DwmRegisterThumbnail
title: DwmRegisterThumbnail function (dwmapi.h)
author: windows-sdk-content
description: Creates a Desktop Window Manager (DWM) thumbnail relationship between the destination and source windows.
old-location: dwm\dwmregisterthumbnail.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmregisterthumbnail.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DwmRegisterThumbnail, DwmRegisterThumbnail function [Desktop Window Manager], _udwm_dwmregisterthumbnail, _udwm_dwmregisterthumbnail_cpp, dwm.dwmregisterthumbnail, dwmapi/DwmRegisterThumbnail, winui._udwm_dwmregisterthumbnail
ms.topic: function
f1_keywords: 
 - "dwmapi/DwmRegisterThumbnail"
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
 - DwmRegisterThumbnail
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DwmRegisterThumbnail function


## -description


Creates a Desktop Window Manager (DWM) thumbnail relationship between the destination and source windows.


## -parameters




### -param hwndDestination

The handle to the window that will use the DWM thumbnail. Setting the destination window handle to anything other than a top-level window type will result in a return value of E_INVALIDARG.


### -param hwndSource

The handle to the window to use as the thumbnail source. Setting the source window handle to anything other than a top-level window type will result in a return value of E_INVALIDARG.


### -param phThumbnailId [out]

A pointer to a handle that, when this function returns successfully, represents the registration of the DWM thumbnail.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Registering a DWM thumbnail relationship will not modify desktop composition; for information about thumbnail positioning, see the documentation for the <a href="https://docs.microsoft.com/windows/desktop/api/dwmapi/nf-dwmapi-dwmupdatethumbnailproperties">DwmUpdateThumbnailProperties</a> function.

The window designated by <i>hwndDestination</i> must either be the desktop window itself or be owned by the process that is calling <b>DwmRegisterThumbnail</b>. This is required to prevent applications from affecting the content of other applications.

The thumbnail registration handle obtained by this function is not globally unique but is unique to the process. Call the <a href="https://docs.microsoft.com/windows/desktop/api/dwmapi/nf-dwmapi-dwmunregisterthumbnail">DwmUnregisterThumbnail</a> function to unregister the thumbnail. This must be done within the process that the relationship was registered in.


#### Examples

The following example demonstrates how to register the desktop thumbnail.


```cpp

HRESULT UpdateDesktop(HWND hwnd)
{
	HRESULT hr = S_OK;

	// Register the thumbnail
	HTHUMBNAIL thumbnail = NULL;

	hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &thumbnail);
	if (SUCCEEDED(hr))
	{
		// Display the thumbnail using DwmUpdateThumbnailProperties
	}
	return hr;	
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/dwm/thumbnail-ovw">DWM Thumbnail Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/dwm/dwm-overview">Desktop Window Manager Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize">DwmQueryThumbnailSourceSize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dwmapi/nf-dwmapi-dwmunregisterthumbnail">DwmUnregisterThumbnail</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dwmapi/nf-dwmapi-dwmupdatethumbnailproperties">DwmUpdateThumbnailProperties</a>
 

 

