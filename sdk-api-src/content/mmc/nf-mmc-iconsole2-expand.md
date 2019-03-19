---
UID: NF:mmc.IConsole2.Expand
title: IConsole2::Expand (mmc.h)
author: windows-sdk-content
description: The IConsole2::Expand method enables the snap-in to expand or collapse an item in the scope pane.
old-location: mmc\iconsole2_expand.htm
tech.root: mmc
ms.assetid: 958c9611-fd9c-4895-903b-145eacf76901
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Expand, Expand method [MMC], Expand method [MMC],IConsole2 interface, IConsole2 interface [MMC],Expand method, IConsole2.Expand, IConsole2::Expand, _slate_iconsole2_expand, mmc.iconsole2_expand, mmc/IConsole2::Expand
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
 - IConsole2.Expand
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsole2::Expand


## -description


The <b>IConsole2::Expand</b> method enables the snap-in to expand or collapse an item in the scope pane.


## -parameters




### -param hItem [in]

A handle to the item to expand.


### -param bExpand [in]

A value that specifies whether to expand or collapse the item. <b>TRUE</b> expands the item. <b>FALSE</b> collapses the item.


## -returns



This method can return one of these values.




## -remarks



The <b>IConsole2::Expand</b> method is the programmatic equivalent of the user clicking on the plus or minus sign to expand or collapse an item in the scope pane. That is, this method causes a visible expansion or collapse of an item in the scope pane. Be aware that this method does not change the selection in the scope pane and does not affect the result pane.

When this method is called, MMC expands or collapses the item specified by <i>hItem</i> based on the value set for <i>bExpand</i>. MMC then sends an expand notification to the snap-in of each child item. MMC does so by calling each child snap-in's 
<a href="https://msdn.microsoft.com/8679396e-23d0-4418-987a-c72b1508e7b9">IComponentData::Notify</a> method with event set to <a href="https://msdn.microsoft.com/de89a195-082b-4d5f-bd8c-1c75215ab60f">MMCN_EXPAND</a>, <i>lpDataObject</i> set as a pointer to the data object for <i>hItem</i>, arg set as <b>TRUE</b> or <b>FALSE</b> based on <i>bExpand</i>, and <i>param</i> set as <i>hItem</i>. Be aware that <i>hItem</i> is the <b>HSCOPEITEM</b> handle that you specified in your call to <b>IConsole2::Expand</b>.

The <b>IConsole2::Expand</b> method applies only to a particular view. This means that it applies only to the instance of the snap-in's 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> object that corresponds to the snap-in item that appears in a specific multiple-document interface (MDI) window within the console. Be aware that each MDI window within the console represents a different view and that an instance of a snap-in within an MDI window corresponds to an 
<b>IComponent</b> object for that snap-in.

Therefore, the snap-in should only call this method on the 
<b>IConsole2</b> interface pointer associated with an 
<b>IComponent</b> object, that is, an 
<b>IConsole2</b> interface pointer retrieved by calling <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">QueryInterface</a> on the <b>IConsole</b> interface pointer returned by 
<a href="https://msdn.microsoft.com/2a8b8f79-05c0-49e8-8210-7c1002ee5978">IComponent::Initialize</a>.

To enumerate the child items of an item in the namespace without visibly expanding the item, the snap-in should use the 
<a href="https://msdn.microsoft.com/3672babb-b172-4f25-8d95-61f3aacce2f0">IConsoleNameSpace2::Expand</a> method.




## -see-also




<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>



<a href="https://msdn.microsoft.com/3672babb-b172-4f25-8d95-61f3aacce2f0">IConsoleNameSpace2::Expand</a>
 

 

