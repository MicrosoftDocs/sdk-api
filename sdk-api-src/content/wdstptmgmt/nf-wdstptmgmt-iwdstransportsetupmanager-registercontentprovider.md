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

# IWdsTransportSetupManager::RegisterContentProvider


## -description


Enables an application run on a client computer to register a content provider DLL. This makes the provider available for use by the WDS transport server.


## -parameters




### -param bszName [in]

The name of the content provider to be registered. This name must be unique on the server. 


### -param bszDescription [in]

A description of the content provider that can be  read by an administrator. 


### -param bszFilePath [in]

The  full path to the DLL that implements the content provider. The path can include environment variables. 


### -param bszInitializationRoutine [in]

The name of a function exported by the content provider that the WDS transport server can use to initialize the provider.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -remarks



To enable a multicast provider to support unauthenticated connections, the provider developer can add the <b>AllowUnAuth</b> key to the registry and set its <b>DWORD</b> value equal to 1.


<b>HKLM</b>\<b>System</b>\<b>CurrentControlSet</b>\<b>Services</b>\<b>WDSServer</b>\<b>Providers</b>\<b>WDSMC</b>\<b>Providers</b>\<b><i>Content Provider Name (i.e. bszName)</i></b>\<b>AllowUnauth</b>






## -see-also




<a href="https://msdn.microsoft.com/b7b0dc9f-081e-472f-98f7-fe555a411ea3">IWdsTransportSetupManager</a>
 

 

