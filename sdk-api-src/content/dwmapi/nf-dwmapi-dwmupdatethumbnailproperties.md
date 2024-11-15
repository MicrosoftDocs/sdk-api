---
UID: NF:dwmapi.DwmUpdateThumbnailProperties
title: DwmUpdateThumbnailProperties function (dwmapi.h)
description: Updates the properties for a Desktop Window Manager (DWM) thumbnail.
helpviewer_keywords: ["DwmUpdateThumbnailProperties","DwmUpdateThumbnailProperties function [Desktop Window Manager]","_udwm_dwmupdatethumbnailproperties","_udwm_dwmupdatethumbnailproperties_cpp","dwm.dwmupdatethumbnailproperties","dwmapi/DwmUpdateThumbnailProperties","winui._udwm_dwmupdatethumbnailproperties"]
old-location: dwm\dwmupdatethumbnailproperties.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmupdatethumbnailproperties.htm
ms.date: 12/05/2018
ms.keywords: DwmUpdateThumbnailProperties, DwmUpdateThumbnailProperties function [Desktop Window Manager], _udwm_dwmupdatethumbnailproperties, _udwm_dwmupdatethumbnailproperties_cpp, dwm.dwmupdatethumbnailproperties, dwmapi/DwmUpdateThumbnailProperties, winui._udwm_dwmupdatethumbnailproperties
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DwmUpdateThumbnailProperties
 - dwmapi/DwmUpdateThumbnailProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dwmapi.dll
api_name:
 - DwmUpdateThumbnailProperties
---

# DwmUpdateThumbnailProperties function


## -description

Updates the properties for a Desktop Window Manager (DWM) thumbnail.

## -parameters

### -param hThumbnailId [in]

The handle to the DWM thumbnail to be updated. Null or invalid thumbnails, as well as thumbnails owned by other processes will result in a return value of E_INVALIDARG.

### -param ptnProperties [in]

A pointer to a <a href="/windows/desktop/api/dwmapi/ns-dwmapi-dwm_thumbnail_properties">DWM_THUMBNAIL_PROPERTIES</a> structure that contains the new thumbnail properties.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Thumbnail relationships created by the <a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmregisterthumbnail">DwmRegisterThumbnail</a> function will not be rendered to the destination window until this function is called. Subsequent calls will update the thumbnail according to the provided properties.


#### Examples

The following example demonstrates how to register and display the desktop thumbnail.


```cpp

HRESULT UpdateDesktop(HWND hwnd)
{
	HRESULT hr = S_OK;

	// Register the thumbnail
	SIZE size = {100,100};
	HTHUMBNAIL thumbnail = NULL;

	hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &size, &thumbnail);
	if (SUCCEEDED(hr))
	{
		// The destination rectangle size
		RECT dest = {0,50,100,150};

		// Set the thumbnail properties for use
		DWM_THUMBNAIL_PROPERTIES dskThumbProps;
		dskThumbProps.dwFlags = DWM_TNP_RECTDESTINATION | DWM_TNP_VISIBLE | DWM_TNP_SOURCECLIENTAREAONLY;

		// Use the window frame and client area
		dskThumbProps.fSourceClientAreaOnly = FALSE;
		dskThumbProps.fVisible = TRUE;
		dskThumbProps.opacity = (255 * 70)/100;
		dskThumbProps.rcDestination = dest;

		// Display the thumbnail
		hr = DwmUpdateThumbnailProperties(thumbnail,&dskThumbProps);
		if (SUCCEEDED(hr))
		{
			// ...
		}
	}
	return hr;	
}
```

## -see-also

<a href="/windows/desktop/dwm/thumbnail-ovw">DWM Thumbnail Overview</a>



<a href="/windows/desktop/dwm/dwm-overview">Desktop Window Manager Overview</a>



<a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmquerythumbnailsourcesize">DwmQueryThumbnailSourceSize</a>



<a href="/windows/desktop/api/dwmapi/nf-dwmapi-dwmunregisterthumbnail">DwmUnregisterThumbnail</a>