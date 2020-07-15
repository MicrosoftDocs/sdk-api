---
UID: NF:mmc.IComponentData.Notify
title: IComponentData::Notify (mmc.h)
description: The IComponentData::Notify method notifies the snap-in of actions performed by the user.
helpviewer_keywords: ["IComponentData interface [MMC]","Notify method","IComponentData.Notify","IComponentData::Notify","Notify","Notify method [MMC]","Notify method [MMC]","IComponentData interface","_slate_icomponentdata_notify","mmc.icomponentdata_notify","mmc/IComponentData::Notify"]
old-location: mmc\icomponentdata_notify.htm
tech.root: mmc
ms.assetid: 8679396e-23d0-4418-987a-c72b1508e7b9
ms.date: 12/05/2018
ms.keywords: IComponentData interface [MMC],Notify method, IComponentData.Notify, IComponentData::Notify, Notify, Notify method [MMC], Notify method [MMC],IComponentData interface, _slate_icomponentdata_notify, mmc.icomponentdata_notify, mmc/IComponentData::Notify
f1_keywords:
- mmc/IComponentData.Notify
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponentData::Notify


## -description


The <b>IComponentData::Notify</b> method notifies the snap-in of actions performed by the user.


## -parameters




### -param lpDataObject [in]

A pointer to the data object of the currently selected item.


### -param event [in]

Identifies an action taken by a user. <b>IComponentData::Notify</b> can receive the following notifications:


<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmcn-btn-click">MMCN_BTN_CLICK</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmcn-delete">MMCN_DELETE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmcn-expand">MMCN_EXPAND</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmcn-expandsync">MMCN_EXPANDSYNC</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmcn-preload">MMCN_PRELOAD</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmcn-property-change">MMCN_PROPERTY_CHANGE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmcn-remove-children">MMCN_REMOVE_CHILDREN</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmcn-rename">MMCN_RENAME</a>



### -param arg [in]

Depends on the notification type.


### -param param [in]

Depends on the notification type.


## -returns



This method can return one of these values.




## -remarks



For more information, see the individual notifications. The snap-in should return <b>S_FALSE</b> for any notification it does not handle.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponent">IComponent</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-icomponentdata">IComponentData</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iconsole2">IConsole2</a>
 

 

