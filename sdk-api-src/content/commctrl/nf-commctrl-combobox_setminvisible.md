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

# ComboBox_SetMinVisible macro


## -description


Sets the minimum number of visible items in the drop-down list of a combo box. 


## -parameters




### -param hwnd

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The combo box. 


### -param iMinVisible

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">INT</a></b>

The minimum number of visible items. 


## -remarks



When the number of items in the drop-down list is greater than the minimum, the combo box uses a scroll bar. By default, 30 is the minimum number of visible items.

<code>Combobox_SetMinVisible (hwnd, iMinVisible)</code>

is equivalent to the following call.

<code>SendMessage((hwnd), CB_SETMINVISIBLE, (WPARAM) iMinVisible, 0);</code>

To use <b>ComboBox_SetMinVisible</b>, the application must specify comctl32.dll version 6 in the manifest. For more information, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 




## -see-also




<a href="https://msdn.microsoft.com/3cf9e488-50ce-4825-acf0-4e665d074f9e">CB_SETMINVISIBLE</a>
 

 

