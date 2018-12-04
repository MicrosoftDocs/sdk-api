---
UID: NF:mmc.IComponentData.Notify
title: IComponentData::Notify
author: windows-sdk-content
description: The IComponentData::Notify method notifies the snap-in of actions performed by the user.
old-location: mmc\icomponentdata_notify.htm
tech.root: mmc
ms.assetid: 8679396e-23d0-4418-987a-c72b1508e7b9
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IComponentData interface [MMC],Notify method, IComponentData.Notify, IComponentData::Notify, Notify, Notify method [MMC], Notify method [MMC],IComponentData interface, _slate_icomponentdata_notify, mmc.icomponentdata_notify, mmc/IComponentData::Notify
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
 - IComponentData.Notify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponentData::Notify


## -description


The <b>IComponentData::Notify</b> method notifies the snap-in of actions performed by the user.


## -parameters




### -param lpDataObject [in]

A pointer to the data object of the currently selected item.


### -param event [in]

Identifies an action taken by a user. <b>IComponentData::Notify</b> can receive the following notifications:


<a href="https://msdn.microsoft.com/166488ab-942f-4e25-9007-b9b79aac5995">MMCN_BTN_CLICK</a>



<a href="https://msdn.microsoft.com/eaf6c7de-2b02-4563-9392-588a74c9d744">MMCN_DELETE</a>



<a href="https://msdn.microsoft.com/de89a195-082b-4d5f-bd8c-1c75215ab60f">MMCN_EXPAND</a>



<a href="https://msdn.microsoft.com/28fbedbf-e7d6-423a-909f-020ff8416cb8">MMCN_EXPANDSYNC</a>



<a href="https://msdn.microsoft.com/a648e5f5-e3da-45d7-8e8f-a3f67699ccdc">MMCN_PRELOAD</a>



<a href="https://msdn.microsoft.com/4b1c6d78-23b1-4b5a-b913-8a7153471785">MMCN_PROPERTY_CHANGE</a>



<a href="https://msdn.microsoft.com/2540fedc-2ee5-44ed-a1bb-4da3eb2146c9">MMCN_REMOVE_CHILDREN</a>



<a href="https://msdn.microsoft.com/1a77e563-e469-466e-b61a-e127dfb19c1a">MMCN_RENAME</a>



### -param arg [in]

Depends on the notification type.


### -param param [in]

Depends on the notification type.


## -returns



This method can return one of these values.




## -remarks



For more information, see the individual notifications. The snap-in should return <b>S_FALSE</b> for any notification it does not handle.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>



<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>
 

 

