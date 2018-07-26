---
UID: NF:mmc.IComponent.QueryDataObject
title: IComponent::QueryDataObject
author: windows-sdk-content
description: The IComponent::QueryDataObject method returns a data object that can be used to retrieve context information for the specified cookie.
old-location: mmc\icomponent_querydataobject.htm
old-project: MMC
ms.assetid: 5bdbd321-4245-4c73-9071-1a9bc3853ba5
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: CCT_RESULT = 0x8001, CCT_SCOPE = 0x8000, CCT_SNAPIN_MANAGER = 0x8002, CCT_UNINITIALIZED = 0xFFFF, IComponent interface [MMC],QueryDataObject method, IComponent.QueryDataObject, IComponent::QueryDataObject, QueryDataObject, QueryDataObject method [MMC], QueryDataObject method [MMC],IComponent interface, _slate_icomponent_querydataobject, mmc.icomponent_querydataobject, mmc/IComponent::QueryDataObject
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - IComponent.QueryDataObject
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IComponent::QueryDataObject


## -description


The <b>IComponent::QueryDataObject</b> method returns a data object that can be used to retrieve context information for the specified cookie.


## -parameters




### -param cookie [in]

A value that specifies the unique identifier for which the data object is required. When called for virtual list items, which do not have cookies, this parameter is set to the item list index.


### -param type [in]

A value that specifies the data object as one of the following.



#### CCT_SCOPE = 0x8000

Data object for the scope item.



#### CCT_RESULT = 0x8001

Data object for the result item.



#### CCT_SNAPIN_MANAGER = 0x8002

Data object for the Snap-In Manager context.



#### CCT_UNINITIALIZED = 0xFFFF

Data object has an invalid type.

These constants are members of the 
<a href="https://msdn.microsoft.com/6f1cb622-b066-4208-9e25-cdd7e9c4dcd2">DATA_OBJECT_TYPES</a> enumeration.


### -param ppDataObject [out]

A pointer to the address of the returned data object.


## -returns



This method can return one of these values.




## -remarks



These data objects can be passed to the same snap-in or to extension snap-ins that require them. Some of the MMC interfaces that can use this data object are 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>, 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>, 
<a href="https://msdn.microsoft.com/3f9a5945-9b34-41fe-9c91-c782eb7eb739">IContextMenuProvider</a>, 
<a href="https://msdn.microsoft.com/8fa4434e-ccdc-43fb-877e-a6f6a5fc95b2">IExtendContextMenu</a>, 
<a href="https://msdn.microsoft.com/9beb0a0a-b3bf-46d0-b10c-0fc3ab25c18d">IExtendPropertySheet2</a>, and 
<a href="https://msdn.microsoft.com/c63d5d5f-a334-4367-8a1e-252b4eb5b50d">IPropertySheetProvider</a>.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/567d068e-5447-438c-9719-93227807263a">IComponentData::QueryDataObject</a>



<a href="https://msdn.microsoft.com/library/ms688421(v=VS.85).aspx">IDataObject</a>
 

 

