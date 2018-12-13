---
UID: NF:mmc.IComponent.Initialize
title: IComponent::Initialize
author: windows-sdk-content
description: The IComponent::Initialize method provides an entry point to the console.
old-location: mmc\icomponent_initialize.htm
tech.root: mmc
ms.assetid: 2a8b8f79-05c0-49e8-8210-7c1002ee5978
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IComponent interface [MMC],Initialize method, IComponent.Initialize, IComponent::Initialize, Initialize, Initialize method [MMC], Initialize method [MMC],IComponent interface, _slate_icomponent_initialize, mmc.icomponent_initialize, mmc/IComponent::Initialize
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
 - IComponent.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IComponent::Initialize


## -description


The <b>IComponent::Initialize</b> method provides an entry point to the console. At this point, the snap-in should set up the toolbar. If the snap-in uses the default list view it should also set up the list view's headers and add images to be used in the result pane.


## -parameters




### -param lpConsole [in]

A pointer to the console 
<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole</a> interface.


## -returns



This method can return one of these values.




## -remarks



<b>IComponent::Initialize</b> is called when a snap-in is being created. The pointer to IConsole that is passed in is used to make QueryInterface calls to the console for interfaces such as 
<a href="https://msdn.microsoft.com/58f8bcdb-b062-4048-92fc-eb652ce62c5b">IResultData</a>. You can also call QueryInterface on the IConsole pointer to get an 
<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/ec4ec242-6376-44e7-bd82-09456789c4c9">IComponent::Destroy</a>



<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>



<a href="https://msdn.microsoft.com/en-us/library/ms688421(v=VS.85).aspx">IDataObject</a>
 

 

