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

# IWMDeviceManager2::Reinitialize


## -description



The <b>Reinitialize</b> method forces Windows Media Device Manager to rediscover all the Windows Media Device Manager devices.




## -parameters






## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



Windows Media Device Manager monitors Plug and Play (PnP) notifications to keep track of connected devices which are controlled by a PnP-compliant service provider. If a non-compliant device is plugged in or some other changes are made to a device for which the device does not generate PnP notifications (for example, insertion or removal of a storage card), the application should call this method before calling <a href="https://msdn.microsoft.com/b5015263-23f2-466f-a89f-26c14f7a2263">IWMDeviceManager2::EnumDevices2</a>. The application would typically do this on a refresh request from the user.




## -see-also




<a href="https://msdn.microsoft.com/ea4bf623-c93a-4c0f-a84f-e3a979b37d60">IWMDeviceManager2 Interface</a>



<a href="https://msdn.microsoft.com/b5015263-23f2-466f-a89f-26c14f7a2263">IWMDeviceManager2::EnumDevices2</a>
 

 

