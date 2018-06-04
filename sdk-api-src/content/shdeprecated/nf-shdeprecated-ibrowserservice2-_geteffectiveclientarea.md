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

# IBrowserService2::_GetEffectiveClientArea


## -description


Deprecated. Used with <a href="https://msdn.microsoft.com/62ede825-a4f3-47bc-a9dd-9b651bde1ec5">IBrowserService2::_GetViewBorderRect</a> to negotiate the dimensions of the browser view.


## -parameters




### -param lprectBorder [in, out]

Type: <b>LPRECT</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure indicating the dimensions of the available client area.


### -param hmon [in]

Type: <b>HMONITOR</b>

The handle of the monitor on which the view is displayed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/c43c1401-52d3-485e-a418-205df5737040">HMONITOR and the Device Context</a>



<a href="https://msdn.microsoft.com/5c100b60-ef2e-4044-9f06-c1d01bcd88d2">IBrowserService2</a>
 

 

