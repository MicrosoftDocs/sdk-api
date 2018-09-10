---
UID: NF:dwmapi.DwmUpdateThumbnailProperties
title: DwmUpdateThumbnailProperties function
author: windows-sdk-content
description: Updates the properties for a Desktop Window Manager (DWM) thumbnail.
old-location: dwm\dwmupdatethumbnailproperties.htm
tech.root: dwm
ms.assetid: VS|winui|~\winui\desktopwindowmanager\reference\functions\dwmupdatethumbnailproperties.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DwmUpdateThumbnailProperties, DwmUpdateThumbnailProperties function [Desktop Window Manager], _udwm_dwmupdatethumbnailproperties, _udwm_dwmupdatethumbnailproperties_cpp, dwm.dwmupdatethumbnailproperties, dwmapi/DwmUpdateThumbnailProperties, winui._udwm_dwmupdatethumbnailproperties
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - DwmUpdateThumbnailProperties
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DwmUpdateThumbnailProperties function


## -description


Updates the properties for a Desktop Window Manager (DWM) thumbnail.


## -parameters




### -param hThumbnailId

The handle to the DWM thumbnail to be updated. Null or invalid thumbnails, as well as thumbnails owned by other processes will result in a return value of E_INVALIDARG.


### -param ptnProperties [in]

A pointer to a <a href="https://msdn.microsoft.com/en-us/library/Aa969502(v=VS.85).aspx">DWM_THUMBNAIL_PROPERTIES</a> structure that contains the new thumbnail properties.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Thumbnail relationships created by the <a href="https://msdn.microsoft.com/en-us/library/Aa969521(v=VS.85).aspx">DwmRegisterThumbnail</a> function will not be rendered to the destination window until this function is called. Subsequent calls will update the thumbnail according to the provided properties.


#### Examples

The following example demonstrates how to register and display the desktop thumbnail.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT UpdateDesktop(HWND hwnd)
{
	HRESULT hr = S_OK;

	// Register the thumbnail
	SIZE size = {100,100};
	HTHUMBNAIL thumbnail = NULL;

	hr = DwmRegisterThumbnail(hwnd, FindWindow(_T("Progman"), NULL), &amp;size, &amp;thumbnail);
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
		hr = DwmUpdateThumbnailProperties(thumbnail,&amp;dskThumbProps);
		if (SUCCEEDED(hr))
		{
			// ...
		}
	}
	return hr;	
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa969541(v=VS.85).aspx">DWM Thumbnail Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa969540(v=VS.85).aspx">Desktop Window Manager Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa969520(v=VS.85).aspx">DwmQueryThumbnailSourceSize</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa969525(v=VS.85).aspx">DwmUnregisterThumbnail</a>
 

 

