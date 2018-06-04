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

# IAMCameraControl::Set


## -description



The <b>Set</b> method sets a specified property on the camera.




## -parameters




### -param Property [in]

Specifies the property to set, as a value from the <a href="https://msdn.microsoft.com/eebf2246-960f-48ea-86b7-7542e69f2e3e">CameraControlProperty</a> enumeration.
          


### -param lValue [in]

Specifies the new value of the property.
          


### -param Flags [in]

Specifies the desired control setting, as a member of the <a href="https://msdn.microsoft.com/806322e7-9a70-4dc1-8b10-2479fb3ec935">CameraControlFlags</a> enumeration.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the <i>Flags</i> parameter is <b>CameraControl_Flags_Auto</b>, the method ignores the <i>lValue</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/f789db78-292e-4092-a5dc-1906845fb1dd">Configure the Video Quality</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/22bc35f1-76d4-4881-91d1-72f05c24561d">IAMCameraControl Interface</a>



<a href="https://msdn.microsoft.com/5a21f207-5fbb-44b2-82d2-89be29dbdf2c">IAMCameraControl::Get</a>
 

 

