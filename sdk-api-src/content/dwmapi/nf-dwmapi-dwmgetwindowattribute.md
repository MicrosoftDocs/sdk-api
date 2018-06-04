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

# DwmGetWindowAttribute function


## -description


Retrieves the current value of a specified attribute applied to a window.


## -parameters




### -param hwnd

The handle to the window from which the attribute data is retrieved.


### -param dwAttribute

The attribute to retrieve, specified as a <a href="https://msdn.microsoft.com/f7ed01d1-b5c6-4071-906b-1647ffa2157c">DWMWINDOWATTRIBUTE</a> value.


### -param pvAttribute [out]

A pointer to a value that, when this function returns successfully, receives the current value of the attribute. The type of the retrieved value depends on the value of the <i>dwAttribute</i> parameter.


### -param cbAttribute

The size of the <a href="https://msdn.microsoft.com/f7ed01d1-b5c6-4071-906b-1647ffa2157c">DWMWINDOWATTRIBUTE</a> value being retrieved. The size is dependent on the type of the <i>pvAttribute</i> parameter.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/51f6544a-edc4-4d0c-b39a-277a8dcbe94f">DwmSetWindowAttribute</a>



<a href="https://msdn.microsoft.com/b728db22-db83-4607-8b09-6967697ef1b0">Enable and Control DWM Composition</a>
 

 

