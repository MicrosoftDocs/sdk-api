---
UID: NF:mmc.IComponent.GetDisplayInfo
title: IComponent::GetDisplayInfo
author: windows-sdk-content
description: The IComponent::GetDisplayInfo method retrieves display information for an item in the result pane.
old-location: mmc\icomponent_getdisplayinfo.htm
old-project: MMC
ms.assetid: 8143d11c-3740-4ffc-88f0-6df779c50521
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetDisplayInfo, GetDisplayInfo method [MMC], GetDisplayInfo method [MMC],IComponent interface, IComponent interface [MMC],GetDisplayInfo method, IComponent.GetDisplayInfo, IComponent::GetDisplayInfo, _slate_icomponent_getdisplayinfo, mmc.icomponent_getdisplayinfo, mmc/IComponent::GetDisplayInfo
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
 - IComponent.GetDisplayInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IComponent::GetDisplayInfo


## -description


The <b>IComponent::GetDisplayInfo</b> method retrieves display information for an item in the result pane.


## -parameters




### -param pResultDataItem [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c8f4682e-e1f7-4f7f-9a56-508648ca8c07">RESULTDATAITEM</a> structure. On input, the mask member specifies the type of data required and the lParam member identifies the item of interest. When called for a virtual list, the nIndex member identifies the desired virtual item and the lParam member is zero.


## -returns



This method can return one of these values.




## -remarks



For virtual lists, MMC calls the 
GetDisplayInfo method only for items that are currently visible in the result pane. This means that 
GetDisplayInfo does not get called for an item until it appears in the result pane.

It is safe to reallocate the memory allocated for members of pResultDataItem only in the following situations:

<ul>
<li>The item is deleted.</li>
<li>
<a href="https://msdn.microsoft.com/ec4ec242-6376-44e7-bd82-09456789c4c9">IComponent::Destroy</a> is called.</li>
<li>GetDisplayInfo is called again for that item.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>



<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>
 

 

