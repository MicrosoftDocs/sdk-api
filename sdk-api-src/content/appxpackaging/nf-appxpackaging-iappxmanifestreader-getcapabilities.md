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

# IAppxManifestReader::GetCapabilities


## -description


Gets the list of capabilities requested by the package.


## -parameters




### -param capabilities [out, retval]

Type: <b><a href="https://msdn.microsoft.com/4912BCB0-424B-40F9-BBD1-3AD0A60B3320">APPX_CAPABILITIES</a>*</b>

The list of capabilities requested by the package. This is a bitwise combination of  the values of the enumeration.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Capabilities are specified using the <a href="https://msdn.microsoft.com/ee6bf220-f139-4ad9-a7a7-e621c189b907">Capability</a> element in the package manifest.

If no package capabilities are defined in the manifest, this method returns <b>S_OK</b> with a zero value.




## -see-also




<a href="https://msdn.microsoft.com/3DA45F2F-7088-4A9B-968C-91E402CAA412">IAppxManifestReader</a>
 

 

