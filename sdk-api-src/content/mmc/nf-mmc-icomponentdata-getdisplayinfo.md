---
UID: NF:mmc.IComponentData.GetDisplayInfo
title: IComponentData::GetDisplayInfo
author: windows-sdk-content
description: The IComponentData::GetDisplayInfo method retrieves display information for a scope item.
old-location: mmc\icomponentdata_getdisplayinfo.htm
old-project: mmc
ms.assetid: bd34652a-8e57-44b4-bbc2-99ffadf2a6cf
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetDisplayInfo, GetDisplayInfo method [MMC], GetDisplayInfo method [MMC],IComponentData interface, IComponentData interface [MMC],GetDisplayInfo method, IComponentData.GetDisplayInfo, IComponentData::GetDisplayInfo, _slate_icomponentdata_getdisplayinfo, mmc.icomponentdata_getdisplayinfo, mmc/IComponentData::GetDisplayInfo
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
 - IComponentData.GetDisplayInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IComponentData::GetDisplayInfo


## -description


The <b>IComponentData::GetDisplayInfo</b> method retrieves display information for a scope item.


## -parameters




### -param pScopeDataItem [in, out]

A pointer to a 
<a href="https://msdn.microsoft.com/c392f25c-80e7-4c91-9063-36143320b9aa">SCOPEDATAITEM</a> structure. On input, the structure mask member specifies the type of information required and the lParam member identifies the item of interest.


## -returns



This method can return one of these values.




## -remarks



It is safe to reallocate the memory allocated for members of the pScopeDataItem parameter only:

<ul>
<li>When the scope item is deleted.</li>
<li>When 
<a href="https://msdn.microsoft.com/adf7238d-b452-499b-8924-2ea1bfecd69f">IComponentData::Destroy</a> is called.</li>
<li>When 
GetDisplayInfo is called again for that scope item.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>



<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>
 

 

