---
UID: NF:mmc.IComponentData.CompareObjects
title: IComponentData::CompareObjects
author: windows-sdk-content
description: The IComponentData::CompareObjects method enables a snap-in to compare two data objects acquired through QueryDataObject. Be aware that the data objects can be acquired from two different instances of IComponentData.
old-location: mmc\icomponentdata_compareobjects.htm
tech.root: mmc
ms.assetid: d6ca3957-3d0c-492d-9e47-fc898981720b
ms.author: windowssdkdev
ms.date: 08/14/2018
ms.keywords: CompareObjects, CompareObjects method [MMC], CompareObjects method [MMC],IComponentData interface, IComponentData interface [MMC],CompareObjects method, IComponentData.CompareObjects, IComponentData::CompareObjects, _slate_icomponentdata_compareobjects, mmc.icomponentdata_compareobjects, mmc/IComponentData::CompareObjects
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
 - IComponentData.CompareObjects
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponentData::CompareObjects


## -description


The <b>IComponentData::CompareObjects</b> method enables a snap-in to compare two data objects acquired through 
<a href="https://msdn.microsoft.com/567d068e-5447-438c-9719-93227807263a">QueryDataObject</a>. Be aware that the data objects can be acquired from two different instances of 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>.


## -parameters




### -param lpDataObjectA [in]

A pointer to the first data object exposing an 
<a href="_ole_idataobject">IDataObject</a> interface that is to be compared.


### -param lpDataObjectB [in]

A pointer to the second data object exposing an <a href="_ole_idataobject">IDataObject</a> interface that is to be compared.


## -returns



This method can return one of these values.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>



<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>
 

 

