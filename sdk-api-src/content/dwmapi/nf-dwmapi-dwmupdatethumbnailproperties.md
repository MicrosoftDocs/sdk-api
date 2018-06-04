---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DwmUpdateThumbnailProperties function


## -description


Updates the properties for a Desktop Window Manager (DWM) thumbnail.


## -parameters




### -param hThumbnailId

The handle to the DWM thumbnail to be updated. Null or invalid thumbnails, as well as thumbnails owned by other processes will result in a return value of E_INVALIDARG.


### -param ptnProperties [in]

A pointer to a <a href="https://msdn.microsoft.com/3dc9676d-c540-4fdf-806b-0feda0ba0371">DWM_THUMBNAIL_PROPERTIES</a> structure that contains the new thumbnail properties.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Thumbnail relationships created by the <a href="https://msdn.microsoft.com/0105b167-9cf0-420d-88a1-2b99cabb4734">DwmRegisterThumbnail</a> function will not be rendered to the destination window until this function is called. Subsequent calls will update the thumbnail according to the provided properties.


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




<a href="https://msdn.microsoft.com/6d71fcda-0cf0-463c-8c60-0415109d154f">DWM Thumbnail Overview</a>



<a href="https://msdn.microsoft.com/fb1e0f1e-a6db-4961-bfa5-9c2218f8c950">Desktop Window Manager Overview</a>



<a href="https://msdn.microsoft.com/279be12c-e993-46e2-aaf8-19747809cb41">DwmQueryThumbnailSourceSize</a>



<a href="https://msdn.microsoft.com/fd14a133-e027-48dd-ae2e-f85652e76e3c">DwmUnregisterThumbnail</a>
 

 

