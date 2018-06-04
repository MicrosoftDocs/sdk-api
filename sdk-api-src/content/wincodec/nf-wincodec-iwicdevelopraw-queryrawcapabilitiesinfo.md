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

# IWICDevelopRaw::QueryRawCapabilitiesInfo


## -description


Retrieves information about which capabilities are supported for a raw image.


## -parameters




### -param pInfo [out]

Type: <b><a href="https://msdn.microsoft.com/1466cd90-8eab-4c5c-bb77-c75d35fe586b">WICRawCapabilitiesInfo</a>*</b>

A pointer that receives <a href="https://msdn.microsoft.com/1466cd90-8eab-4c5c-bb77-c75d35fe586b">WICRawCapabilitiesInfo</a> that provides the capabilities supported by the raw image.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



It is recommended that a codec report that a capability is supported even if the results at the outer range limits are not of perfect quality.



