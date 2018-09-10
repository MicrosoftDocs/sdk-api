---
UID: NF:mmc.IComponent.CompareObjects
title: IComponent::CompareObjects
author: windows-sdk-content
description: The IComponent::CompareObjects method enables a snap-in to compare two data objects acquired through IComponent::QueryDataObject. Be aware that data objects can be acquired from two different instances of IComponent.
old-location: mmc\icomponent_compareobjects.htm
tech.root: mmc
ms.assetid: 5bd7cd8e-140c-4f7b-9f2b-bf1bfe8a9a7a
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: CompareObjects, CompareObjects method [MMC], CompareObjects method [MMC],IComponent interface, IComponent interface [MMC],CompareObjects method, IComponent.CompareObjects, IComponent::CompareObjects, _slate_icomponent_compareobjects, mmc.icomponent_compareobjects, mmc/IComponent::CompareObjects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - Mmc.h
api_name:
 - IComponent.CompareObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponent::CompareObjects


## -description


The <b>IComponent::CompareObjects</b> method enables a snap-in to compare two data objects acquired through 
<a href="https://msdn.microsoft.com/5bdbd321-4245-4c73-9071-1a9bc3853ba5">IComponent::QueryDataObject</a>. Be aware that data objects can be acquired from two different instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>.


## -parameters




### -param lpDataObjectA [in]

A pointer to the first object exposing an IDataObject interface that is to be compared.


### -param lpDataObjectB [in]

A pointer to the second object exposing an IDataObject interface that is to be compared.


## -returns



This method can return one of these values.




## -remarks



The 
IDataObject interface is documented in the Platform Software Development Kit (SDK).




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>



<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>
 

 

