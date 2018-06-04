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

# IDXGIDisplayControl::IsStereoEnabled


## -description


Retrieves a Boolean value that indicates whether the operating system's stereoscopic 3D display behavior is enabled.


## -parameters






## -returns



<b>IsStereoEnabled</b> returns TRUE when the operating system's stereoscopic 3D display behavior is enabled and FALSE when this behavior is disabled.

<b>Platform Update for Windows 7:  </b>On Windows 7 or Windows Server 2008 R2 with the <a href="http://support.microsoft.com/kb/2670838">Platform Update for Windows 7</a> installed, <b>IsStereoEnabled</b> always returns FALSE because stereoscopic 3D display behavior isn’t available with the Platform Update for Windows 7. For more info about the Platform Update for Windows 7, see <a href="https://msdn.microsoft.com/C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1">Platform Update for Windows 7</a>. 




## -remarks



You pass a Boolean value to the  <a href="https://msdn.microsoft.com/4A449444-287D-4F1D-9A86-F6165C38048F">IDXGIDisplayControl::SetStereoEnabled</a> method to either enable or disable the operating system's stereoscopic 3D display behavior. TRUE enables the operating system's stereoscopic 3D display behavior and FALSE disables it.




## -see-also




<a href="https://msdn.microsoft.com/8E9A059E-D7E2-4179-9ECA-D66BC9CD3757">IDXGIDisplayControl</a>
 

 

