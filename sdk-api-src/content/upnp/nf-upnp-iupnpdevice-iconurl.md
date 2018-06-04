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

# IUPnPDevice::IconURL


## -description


The 
<b>IconURL</b> method returns a URL from which an icon of the specified format can be loaded.


## -parameters




### -param bstrEncodingFormat [in]

Specifies the MIME type of the encoding format that is requested for the icon.


### -param lSizeX [in]

Specifies the width of the icon, in pixels. Standard values are 16, 32, or 48.


### -param lSizeY [in]

Specifies the height of the icon, in pixels. Standard values are 16, 32, or 48 pixels.


### -param lBitDepth [in]

Specifies the bit depth of the icon. Standard values are 8, 16, or 24.


### -param pbstrIconURL [out]

Receives a reference to a string that contains the URL from which the icon is to be loaded. Release this string with <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when it is no longer required.


## -returns



If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.




## -remarks



An application can specify any values for <i>lSizeX</i>, <i>lSizeY</i>, and <i>lBitDepth</i>. However, there is no guarantee that an icon exists with those specifications.

If a matching icon does not exist, the URL for the icon that most closely matches the size and bit depth specified is returned.




## -see-also




<a href="https://msdn.microsoft.com/566cc606-3dfb-4052-93b0-3c922bf30f84">IUPnPDevice</a>
 

 

