---
UID: NF:mmc.IConsole.UpdateAllViews
title: IConsole::UpdateAllViews
author: windows-sdk-content
description: Called by a snap-in when there is a content change in the result pane. This method can be called either by IComponent or IComponentData.
old-location: mmc\iconsole_updateallviews.htm
tech.root: mmc
ms.assetid: 72A0FFF3-4084-4AD0-94E4-A7EB03F40BF2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IConsole interface [MMC],UpdateAllViews method, IConsole.UpdateAllViews, IConsole::UpdateAllViews, UpdateAllViews, UpdateAllViews method [MMC], UpdateAllViews method [MMC],IConsole interface, mmc.iconsole_updateallviews, mmc/IConsole::UpdateAllViews
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
req.idl: Mmc.idl
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
 - IConsole.UpdateAllViews
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IConsole::UpdateAllViews


## -description


Called by a snap-in when there is a content change in the result pane. This method can be called either by 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> or 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>.


## -parameters




### -param lpDataObject [in]

A pointer to a user-supplied data object.


### -param data [in]

A user-defined value, for example a pointer to the modified content.


### -param hint [in]

A user-defined value, for example information about the type of content change.


## -returns



This method can return one of these values.




## -remarks



This method sends an <a href="https://msdn.microsoft.com/3c76e700-0162-41ec-8f9d-45a03e6f5956">MMCN_VIEW_CHANGE</a> notification to all instances of 
<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a> associated with the snap-in instance calling this method. The <i>lpDataObject</i>, <i>data</i>, and <i>hint</i> parameters are passed as the <i>lpDataObject</i> arg, and param for the 
<a href="https://msdn.microsoft.com/38c3b31f-356c-46cf-904a-98241c0f199f">IComponent::Notify</a> method.

This method should be called from the 
<a href="https://msdn.microsoft.com/edd98f5e-e251-40ff-8136-02bf1b9ea670">IConsole</a> interface pointer obtained through the snap-in 
<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a> implementation.




## -see-also




<a href="https://msdn.microsoft.com/edd98f5e-e251-40ff-8136-02bf1b9ea670">IConsole</a>



<a href="https://msdn.microsoft.com/cf9c9fe9-f58f-47f0-9051-86a514df0c6d">IToolbar</a>
 

 

