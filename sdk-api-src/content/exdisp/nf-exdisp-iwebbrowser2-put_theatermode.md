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

# IWebBrowser2::put_TheaterMode


## -description


Sets or gets whether the object is in theater mode.

This property is read/write.


## -parameters


## -remarks



In theater mode, the object's main window fills the entire screen and displays a toolbar that has a minimal set of navigational buttons. A status bar is also provided in the upper-right corner of the screen. Explorer bars, such as  History  and Favorites , are displayed as an autohide pane on the left edge of the screen in theater mode. 

Setting TheaterMode (even to VARIANT_FALSE) resets the values of the IWebBrowser2::AddressBar and IWebBrowser2::ToolBar properties to VARIANT_TRUE. Disable the address bar and toolbars after you set the TheaterMode property. 

The WebBrowser object saves the value of this property, but otherwise ignores it. 




## -see-also




<a href="https://msdn.microsoft.com/AFED694C-8D7B-4539-9A1A-B2DA546F3A07">IWebBrowser2</a>
 

 

