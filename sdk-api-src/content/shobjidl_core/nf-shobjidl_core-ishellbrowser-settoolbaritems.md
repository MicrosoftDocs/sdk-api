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

# IShellBrowser::SetToolbarItems


## -description


<p class="CCE_Message">[This method has no effect on Windows Vista or later operating systems.]

Adds toolbar items to Windows Explorer's toolbar.


## -parameters




### -param lpButtons

Type: <b>LPTBBUTTONSB</b>

The address of an array of <a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a> structures.


### -param nButtons

Type: <b>UINT</b>

The number of <a href="https://msdn.microsoft.com/c7dea982-d8b3-44e1-a4d2-3cca560c2096">TBBUTTON</a> structures in the <i>lpButtons</i> array.


### -param uFlags

Type: <b>UINT</b>

Flags specifying where the toolbar buttons should go. This parameter can be one or more of the following values.



#### FCT_ADDTOEND

Add at the right side of the toolbar.



#### FCT_CONFIGABLE

Not implemented.



#### FCT_MERGE

Merge the toolbar items instead of replacing all of the buttons with those provided by the view. This is the recommended choice.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or a COM-defined error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/138d90e3-a1f0-4faf-88ca-16c7a46df0ca">IShellBrowser</a>
 

 

