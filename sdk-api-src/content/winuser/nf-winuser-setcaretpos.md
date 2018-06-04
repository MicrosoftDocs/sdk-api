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

# SetCaretPos function


## -description


Moves the caret to the specified coordinates. If the window that owns the caret was created with the <b>CS_OWNDC</b> class style, then the specified coordinates are subject to the mapping mode of the device context associated with that window. 


## -parameters




### -param X [in]

Type: <b>int</b>

The new x-coordinate of the caret. 


### -param Y [in]

Type: <b>int</b>

The new y-coordinate of the caret. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. 




## -remarks



<b>SetCaretPos</b> moves the caret whether the caret is hidden. 

The system provides one caret per queue. A window should create a caret only when it has the keyboard focus or is active. The window should destroy the caret before losing the keyboard focus or becoming inactive. A window can set the caret position only if it owns the caret. 

<h3><a id="DPI_Virtualization"></a><a id="dpi_virtualization"></a><a id="DPI_VIRTUALIZATION"></a>DPI Virtualization</h3>
This API does not participate in DPI virtualization. The provided position is interpreted as logical coordinates in terms of the window associated with the caret. The calling thread is not taken into consideration.


#### Examples

For an example, see <a href="using_carets.htm">Creating and Displaying a Caret</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/34ff3420-a1d2-46cc-9378-4b3340bec8c8">Carets</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/14786dc7-bdd2-45e5-8073-b8dc3f5d30de">GetCaretPos</a>



<a href="https://msdn.microsoft.com/2fab919f-11aa-429e-aaa6-89854caa7b1c">HideCaret</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/1a3a141e-9b5a-495a-8138-b9522933499f">ShowCaret</a>
 

 

