---
UID: NE:activationregistration.InstancingType
title: InstancingType
author: windows-sdk-content
description: Represents the kind of instancing behavior for the out-of-process server.
old-location: winrt\instancingtype.htm
old-project: WinRT
ms.assetid: 42E6A5EE-06B0-4F38-92D0-729922AD9FFF
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: InstancingType, InstancingType enumeration [Windows Runtime], MultipleInstances, SingleInstance, activationregistration/InstancingType, activationregistration/MultipleInstances, activationregistration/SingleInstance, winrt.instancingtype
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: activationregistration.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Activation.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InstancingType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - activationregistration.h
api_name:
 - InstancingType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# InstancingType enumeration


## -description


Represents the kind of  instancing behavior for the out-of-process server.


## -enum-fields




### -field InstancingType_SingleInstance


### -field InstancingType_MultipleInstances


### -field int




#### - MultipleInstances

Create more than one instance of the out-of-process server.


#### - SingleInstance

Create a singleton instance of the out-of-process server.


## -see-also




<a href="https://msdn.microsoft.com/1D8F7B12-2883-478D-B83D-84AC47D512E4">IExeServerActivatableClassRegistration</a>



<a href="https://msdn.microsoft.com/9A96968D-B9BD-4C47-B626-69B6EA6AE7EA">IExeServerRegistration</a>
 

 

