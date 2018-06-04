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

# IWindowsDevicesAllJoynBusAttachmentFactoryInterop::alljoyn


## -description


Constructs an <b>AllJoynBusAttachment</b> over an existing <b>alljoyn_busattachment</b> instance without taking ownership.


## -parameters




### -param win32handle [in]

The Win32 handle for the existing instance.


### -param enableAboutData [in]

Toggle to enable AboutData. 


### -param riid [in]

The ID of the <b>IAllJoynBusAttachment</b> interface.


### -param ppv [out]

Out parameter through which the  <b>AllJoynBusAttachment</b> is returned.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code. 




## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable </a>



<a href="https://msdn.microsoft.com/2E9FE6B4-E8F0-4627-A712-F7A4CE5404BE">IWindowsDevicesAllJoynBusAttachmentFactoryInterop</a>
 

 

