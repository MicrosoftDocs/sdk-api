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

# tagHH_POPUP structure


## -description


Use this structure to specify or modify the attributes of a pop-up window. 


## -struct-fields




### -field cbStruct

Specifies the size of the structure. This value must always be filled in before passing the structure to HtmlHelp(). 


### -field hinst

Instance handle of the program or DLL to retrieve the string resource from. Ignored if <i>idString</i> is zero, or if <i>idString</i> specifies a file name. 


### -field idString

Specifies zero, a resource ID, or a topic number in a text file. 


### -field pszText

Specifies the text to display if <i>idString</i> is zero. 


### -field pt

Specifies (in pixels) where the top center of the pop-up window should be located. 


### -field clrForeground

Specifies the RGB value to use for the foreground color of the pop-up window. To use the system color for the window text, specify -1. 


### -field clrBackground

Specifies the RGB value to use for the background color of the pop-up window. To use the system color for the window background, specify -1. 


### -field rcMargins

Specifies (in pixels) the margins to use on the left, top, right, and bottom sides of the pop-up window. The default for all rectangle members is -1. 


### -field pszFont

Specifies the font attributes to use for the text in the pop-up window.


Use the following format to specify font family, point size, character set, and font format:

facename[, point size[, charset[ BOLD ITALIC UNDERLINE]]]

To omit an attribute, enter a comma. For example, to specify bold, 10-pt, MS Sans Serif font, <i>pszFont</i> would be:

MS Sans Serif, 10, , BOLD 


## -see-also




<a href="https://msdn.microsoft.com/E75CA82E-9759-47d8-AF84-5842EDAB019D">About Structures</a>
 

 

