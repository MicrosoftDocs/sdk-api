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

# IWindowsDevicesAllJoynBusAttachmentInterop::alljoyn


## -description


Classic COM interface that simply returns a pointer to the underlying <b>alljoyn_busattachment</b> instance, so the app can use it directly with the AllJoyn Core C API.


## -parameters




### -param value [out]

The pointer to the underlying alljoyn_busattachment instance.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code. 





## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable </a>



<a href="https://msdn.microsoft.com/F08A2D95-A84E-47C9-9485-98306993DB52">IWindowsDevicesAllJoynBusAttachmentInterop</a>
 

 

