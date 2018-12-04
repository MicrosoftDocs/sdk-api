---
UID: NF:sbtsv.ITsSbProvider.CreateTargetPropertySetObject
title: ITsSbProvider::CreateTargetPropertySetObject
author: windows-sdk-content
description: Creates an ITsSbTargetPropertySet target property set object.
old-location: termserv\itssbprovider_createtargetpropertysetobject.htm
tech.root: termserv
ms.assetid: 82e9d414-2137-44f3-a984-dc12aba3ecd9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: CreateTargetPropertySetObject, CreateTargetPropertySetObject method [Remote Desktop Services], CreateTargetPropertySetObject method [Remote Desktop Services],ITsSbProvider interface, ITsSbProvider interface [Remote Desktop Services],CreateTargetPropertySetObject method, ITsSbProvider.CreateTargetPropertySetObject, ITsSbProvider::CreateTargetPropertySetObject, sbtsv/ITsSbProvider::CreateTargetPropertySetObject, termserv.itssbprovider_createtargetpropertysetobject
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: sbtsv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Sbtsv.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sbtsv.h
api_name:
 - ITsSbProvider.CreateTargetPropertySetObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITsSbProvider::CreateTargetPropertySetObject


## -description


Creates an <a href="https://msdn.microsoft.com/74ea8132-cb06-40ce-b3bf-4bd8babe3711">ITsSbTargetPropertySet</a> target property set object.


## -parameters




### -param ppPropertySet [out]

A pointer to a pointer to an <a href="https://msdn.microsoft.com/74ea8132-cb06-40ce-b3bf-4bd8babe3711">ITsSbTargetPropertySet</a> property set object. When you have finished using the object, release it by calling the <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a> method. Because RD Connection Broker is unaware of the contents of the property set object, you should clean the object before calling its <b>Release</b> method.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Plug-ins can use this method to create a target property set object.




## -see-also




<a href="https://msdn.microsoft.com/a8574750-d86e-4b0d-a534-d005596e2a33">ITsSbProvider</a>



<a href="https://msdn.microsoft.com/74ea8132-cb06-40ce-b3bf-4bd8babe3711">ITsSbTargetPropertySet</a>
 

 

