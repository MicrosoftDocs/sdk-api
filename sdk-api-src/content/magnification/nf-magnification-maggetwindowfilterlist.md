---
UID: NF:magnification.MagGetWindowFilterList
title: MagGetWindowFilterList function
author: windows-sdk-content
description: Retrieves the list of windows that are magnified or excluded from magnification.
old-location: magapi\magapi_MagGetWindowFilterList.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\maggetwindowfilterlist.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: MagGetWindowFilterList, MagGetWindowFilterList function [Magnification API], magapi.magapi_MagGetWindowFilterList, magapi_MagGetWindowFilterList, magnification/MagGetWindowFilterList
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: magnification.h
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
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagGetWindowFilterList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MagGetWindowFilterList function


## -description


Retrieves the list of windows that are magnified or excluded from magnification.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param pdwFilterMode [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The filter mode, as set by <a href="https://msdn.microsoft.com/en-us/library/ms692396(v=VS.85).aspx">MagSetWindowFilterList</a>.


### -param count [in]

Type: <b>int</b>

The number of windows to retrieve, or 0 to retrieve a count of windows in the filter list.


### -param pHWND [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>*</b>

The list of window handles.


## -returns



Type: <b>int</b>

Returns the count of window handles in the filter list, or -1 if the <i>hwnd</i> parameter is not valid. 




## -remarks



First call the method with a <i>count</i> of 0 to retrieve the count of windows in the filter list. Use the retrieved count to allocate
			sufficient memory for the retrieved list of window handles.

This function requires Windows Display Driver Model (WDDM)-capable video cards.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms692396(v=VS.85).aspx">MagSetWindowFilterList</a>
 

 

