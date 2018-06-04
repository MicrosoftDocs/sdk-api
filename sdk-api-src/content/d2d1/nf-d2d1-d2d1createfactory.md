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

# D2D1CreateFactory function


## -description


Creates a factory object 
  that can be used to create Direct2D resources.


## -parameters




### -param factoryType [in]

Type: <b><a href="https://msdn.microsoft.com/428053d3-7ea0-4b01-9924-4a31d8e018fb">D2D1_FACTORY_TYPE</a></b>

The threading model of the factory and the resources it creates.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a> that is obtained by using __uuidof(ID2D1Factory).


### -param pFactoryOptions [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/2765d34e-978c-4121-82c9-2780d54e2850">D2D1_FACTORY_OPTIONS</a>*</b>

The level of detail provided to the debugging layer.


### -param ppIFactory [out]

Type: <b>void**</b>

When this method returns, contains the address to a pointer to the new factory.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a> interface provides the starting point for  Direct2D. In general, objects created from a single instance of a factory object can be used with other resources created from that instance, but not with resources created by other factory instances.  
	 




## -see-also




<a href="https://msdn.microsoft.com/b1362ef6-40fc-4fa5-ba5b-22c622c39f04">Direct2D API Overview</a>
 

 

