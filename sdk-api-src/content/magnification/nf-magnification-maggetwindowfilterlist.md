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

# MagGetWindowFilterList function


## -description


Retrieves the list of windows that are magnified or excluded from magnification.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param pdwFilterMode [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a>*</b>

The filter mode, as set by <a href="https://msdn.microsoft.com/7f640959-6d50-4742-aace-1b4f13ca472f">MagSetWindowFilterList</a>.


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




<a href="https://msdn.microsoft.com/7f640959-6d50-4742-aace-1b4f13ca472f">MagSetWindowFilterList</a>
 

 

