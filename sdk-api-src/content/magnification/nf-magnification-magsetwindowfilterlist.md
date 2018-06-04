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

# MagSetWindowFilterList function


## -description


Sets the list of windows to be magnified or the 
		list of windows to be excluded from magnification.


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the magnification window.


### -param dwFilterMode [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The magnification filter mode. It can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>MW_FILTERMODE_INCLUDE</td>
<td>Magnify the windows.
<div class="alert"><b>Note</b>  This value is not supported on Windows 7 or Windows 8.</div>
<div> </div>


</td>
</tr>
<tr>
<td>MW_FILTERMODE_EXCLUDE</td>
<td>Exclude the windows from magnification.</td>
</tr>
</table>
 


### -param count [in]

Type: <b>int</b>

The number of window handles in the list.


### -param pHWND [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>*</b>

The list of window handles.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



This function requires Windows Display Driver Model (WDDM)-capable video cards.

Only one window list is used. You can specify either MW_FILTERMODE_INCLUDE or MW_FILTERMODE_EXCLUDE, 
		depending on whether it is more convenient to list included windows or excluded windows.

The magnification window itself is automatically excluded.




## -see-also




<a href="https://msdn.microsoft.com/a2f7beaa-12fd-4363-a9a2-4d564158dda1">MagGetWindowFilterList</a>
 

 

