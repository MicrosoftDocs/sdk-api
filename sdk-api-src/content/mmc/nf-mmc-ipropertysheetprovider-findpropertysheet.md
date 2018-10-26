---
UID: NF:mmc.IPropertySheetProvider.FindPropertySheet
title: IPropertySheetProvider::FindPropertySheet
author: windows-sdk-content
description: Determines whether a specific property sheet exists.
old-location: mmc\ipropertysheetprovider_findpropertysheet.htm
tech.root: mmc
ms.assetid: 14f3a2b7-9e14-4068-a85a-20c41d7e4a4d
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: FindPropertySheet, FindPropertySheet method [MMC], FindPropertySheet method [MMC],IPropertySheetProvider interface, IPropertySheetProvider interface [MMC],FindPropertySheet method, IPropertySheetProvider.FindPropertySheet, IPropertySheetProvider::FindPropertySheet, _slate_ipropertysheetprovider_findpropertysheet, mmc.ipropertysheetprovider_findpropertysheet, mmc/IPropertySheetProvider::FindPropertySheet
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
req.dll: Mmcndmgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IPropertySheetProvider.FindPropertySheet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertySheetProvider::FindPropertySheet


## -description


The <b>IPropertySheetProvider::FindPropertySheet</b> method determines whether a specific property sheet exists.


## -parameters




### -param hItem

TBD


### -param lpComponent [in]

A pointer to the 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> interface on the selected object. <b>NULL</b> if the object selected is a folder (on the scope or result panes), and  
<b>IComponent</b> of the snap-in if it is a result pane leaf item.


### -param lpDataObject [in]

A pointer to the 
<a href="_ole_idataobject">IDataObject</a> interface on the data object.


#### - HSCOPEITEM

A handle to the selected item in the scope pane.



## -returns



This method can return one of these values.




## -remarks



Items in the scope pane are owned by the console so there is no need to interact with the 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> interface. The snap-in must implement 
<a href="https://msdn.microsoft.com/5bd7cd8e-140c-4f7b-9f2b-bf1bfe8a9a7a">IComponent::CompareObjects</a> or 
<a href="https://msdn.microsoft.com/d6ca3957-3d0c-492d-9e47-fc898981720b">IComponentData::CompareObjects</a> to compare the data object with other data objects for existing property sheets.




## -see-also




<a href="https://msdn.microsoft.com/c63d5d5f-a334-4367-8a1e-252b4eb5b50d">IPropertySheetProvider</a>
 

 

