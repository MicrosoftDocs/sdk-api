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

# IPortableDeviceServiceCapabilities::GetFormatRenderingProfiles


## -description


The <b>GetFormatRenderingProfiles</b> method retrieves the rendering profiles of a format.


## -parameters




### -param Format [in]

The format whose rendering profiles are retrieved.


### -param ppRenderingProfiles [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597598">IPortableDeviceValuesCollection</a> object that receives the list of rendering profiles.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



The rendering profiles are similar to what the <a href="https://msdn.microsoft.com/library/windows/hardware/ff597881">WPD_FUNCTIONAL_CATEGORY_RENDERING_INFORMATION</a> functional object returns for device-wide rendering profiles, so that the <b>DisplayRenderingProfile</b> helper function described in <a href="https://msdn.microsoft.com/2332e3cc-087c-49cf-bde9-7f86f65158e7">Retrieving the Rendering Capabilities Supported by a Device</a> could be used here as well.    But there are differences: The <b>GetFormatRenderingProfiles</b> method retrieves only rendering profiles that apply to the selected service and have been filtered by format.




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

