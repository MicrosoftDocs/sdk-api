---
UID: NF:mmc.IComponent.Notify
title: IComponent::Notify (mmc.h)
author: windows-sdk-content
description: The IComponent::Notify method notifies the snap-in of actions taken by the user.
old-location: mmc\icomponent_notify.htm
tech.root: mmc
ms.assetid: 38c3b31f-356c-46cf-904a-98241c0f199f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComponent interface [MMC],Notify method, IComponent.Notify, IComponent::Notify, Notify, Notify method [MMC], Notify method [MMC],IComponent interface, _slate_icomponent_notify, mmc.icomponent_notify, mmc/IComponent::Notify
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
 - IComponent.Notify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponent::Notify


## -description


The <b>IComponent::Notify</b> method notifies the snap-in of actions taken by the user.


## -parameters




### -param lpDataObject [in]

A pointer to the data object of the currently selected item.


### -param event [in]

Identifies an action taken by a user. <b>IComponent::Notify</b> can receive the following notifications:


<a href="https://msdn.microsoft.com/51aa4709-6e33-41eb-958a-108fec6865b4">MMCN_ACTIVATE</a>



<a href="https://msdn.microsoft.com/26f4b8da-f490-4b8d-8016-1aa50dd21f62">MMCN_ADD_IMAGES</a>



<a href="https://msdn.microsoft.com/166488ab-942f-4e25-9007-b9b79aac5995">MMCN_BTN_CLICK</a>



<a href="https://msdn.microsoft.com/92e98c31-032c-48ca-ba1c-a4062b208d6d">MMCN_COLUMN_CLICK</a>



<a href="https://msdn.microsoft.com/634f14ba-0b6a-41b6-af97-e957d1337623">MMCN_COLUMNS_CHANGED</a>



<a href="https://msdn.microsoft.com/e12616c0-e5bc-4a0d-8199-467c1647acf6">MMCN_CONTEXTHELP</a>



<a href="https://msdn.microsoft.com/0c85cd06-4799-4bb6-aa1d-3386edbf1a37">MMCN_DBLCLICK</a>



<a href="https://msdn.microsoft.com/eaf6c7de-2b02-4563-9392-588a74c9d744">MMCN_DELETE</a>



<a href="https://msdn.microsoft.com/54a491a2-35bd-4650-a912-527ee7af78c5">MMCN_DESELECT_ALL</a>



<a href="https://msdn.microsoft.com/82a1d00a-5787-4fad-b3c5-cbcf51a25338">MMCN_FILTERBTN_CLICK</a>



<a href="https://msdn.microsoft.com/b779f04c-1129-4e05-83c5-fd15ff72f1c2">MMCN_FILTER_CHANGE</a>



<a href="https://msdn.microsoft.com/79256d4a-a936-419e-a953-80d743d05290">MMCN_INITOCX</a>



<a href="https://msdn.microsoft.com/ce2a3146-f466-4768-a573-a4968baf659e">MMCN_LISTPAD</a>



<a href="https://msdn.microsoft.com/54fccd83-aa89-4b9d-a9fe-145b850f455c">MMCN_MINIMIZED</a>



<a href="https://msdn.microsoft.com/a2eedeb8-663a-43eb-9b8b-ab419a8b3f79">MMCN_PASTE</a>



<a href="https://msdn.microsoft.com/74814817-f93b-476f-a477-e6b65ed229bb">MMCN_PRINT</a>



<a href="https://msdn.microsoft.com/4b1c6d78-23b1-4b5a-b913-8a7153471785">MMCN_PROPERTY_CHANGE</a>



<a href="https://msdn.microsoft.com/19259852-be87-40f6-8475-26f7cc232db6">MMCN_QUERY_PASTE</a>



<a href="https://msdn.microsoft.com/c39d99f7-7e80-4bad-8494-41f7f28c83a3">MMCN_REFRESH</a>



<a href="https://msdn.microsoft.com/1a77e563-e469-466e-b61a-e127dfb19c1a">MMCN_RENAME</a>



<a href="https://msdn.microsoft.com/5b6c6d7c-af9f-4773-b9b1-1e11f4a1c1f8">MMCN_RESTORE_VIEW</a>



<a href="https://msdn.microsoft.com/ca3a39ee-da6d-46bc-ac75-4afd89cc8565">MMCN_SELECT</a>



<a href="https://msdn.microsoft.com/cc2a9da4-1351-4930-8fb4-577cdcc14e10">MMCN_SHOW</a>



<a href="https://msdn.microsoft.com/6d2f8870-7f06-48f3-aa76-09e99d2c6858">MMCN_SNAPINHELP</a>



<a href="https://msdn.microsoft.com/3c76e700-0162-41ec-8f9d-45a03e6f5956">MMCN_VIEW_CHANGE</a>



### -param arg

Depends on the notification type.


### -param param

Depends on the notification type.


## -returns



This method can return one of these values.




## -remarks



For more information, see the individual notifications. The snap-in should return <b>S_FALSE</b> for any notification it does not handle.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>



<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>



<a href="https://msdn.microsoft.com/124656df-5d12-4de1-9a71-ba080ef36611">IExtendControlbar::ControlbarNotify</a>
 

 

