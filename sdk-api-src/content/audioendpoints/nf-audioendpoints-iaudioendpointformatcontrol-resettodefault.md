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

# IAudioEndpointFormatControl::ResetToDefault


## -description


Resets the format to the default setting provided by the device manufacturer.


## -parameters




### -param ResetFlags [in]

Allows the application to specify which formats are reset.  If
                      no flags are set, then this method reevaluates both the endpoint's 
    device format and mix format and sets them to their default values.

ENDPOINT_FORMAT_RESET_MIX_ONLY: Only reset the mix format.  The endpoint's device
    format will not be reset if this flag is set.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7FF7DCF2-0580-4B50-8EA9-87DB9478B1E8">IAudioEndpointFormatControl</a>
 

 

