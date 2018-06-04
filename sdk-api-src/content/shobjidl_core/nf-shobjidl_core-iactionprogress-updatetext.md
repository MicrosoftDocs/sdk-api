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

# IActionProgress::UpdateText


## -description


Called if descriptive text associated with the action will be changed.


## -parameters




### -param sptext [in]

Type: <b><a href="https://msdn.microsoft.com/3d33cb3a-5949-446c-97ec-7ac4f4b1f675">SPTEXT</a></b>

A value that specifies the type of text displayed. See <a href="https://msdn.microsoft.com/3d33cb3a-5949-446c-97ec-7ac4f4b1f675">SPTEXT</a> for acceptable values.


### -param pszText [in]

Type: <b>LPCWSTR</b>

A pointer to a wide character string to display.


### -param fMayCompact [in]

Type: <b>BOOL</b>

A value that specifies whether to allow a text string to be compacted to fit the available space on screen.


## -returns



Type: <b>HRESULT</b>

Return S_OK if successful, or an error value otherwise.




## -remarks




		The class implementing this method must interpret the value of <i>sptext</i> and <i>fMayCompact</i> in the context of the action being performed and the UI that shows the progress to the user. The value of <i>sptext</i> can be used to differentiate between lines of changeable text. Often, the value of <i>fMayCompact</i> refers to whether the text string can be truncated with an ellipsis (...) in order to conserve screen space.
		




## -see-also




<a href="https://msdn.microsoft.com/e742e381-0fd2-482a-81a0-7b43d11b073b">IActionProgress</a>



<a href="https://msdn.microsoft.com/3d33cb3a-5949-446c-97ec-7ac4f4b1f675">SPTEXT</a>
 

 

