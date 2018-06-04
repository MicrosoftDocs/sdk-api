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

# IMFImageSharingEngine::GetDevice


## -description


Gets information about the image sharing device.


## -parameters




### -param pDevice [out]

A pointer to a <a href="https://msdn.microsoft.com/B006298C-B733-4E76-BD31-A3D1DD4DC766">DEVICE_INFO</a> structure. The method fills in this structure with the device information.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The method allocates memory for the <b>BSTR</b> members of the <a href="https://msdn.microsoft.com/B006298C-B733-4E76-BD31-A3D1DD4DC766">DEVICE_INFO</a> structure. The caller must free the memory for each <b>BSTR</b> by calling <b>SysFreeString</b>.




## -see-also




<a href="https://msdn.microsoft.com/A30C73DA-9BD5-4D12-A6FB-771BBD2D1191">IMFImageSharingEngine</a>
 

 

