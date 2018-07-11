---
UID: NF:mmc.IComponentData.Initialize
title: IComponentData::Initialize
author: windows-sdk-content
description: The IComponentData::Initialize method provides an entry point to the console.
old-location: mmc\icomponentdata_initialize.htm
old-project: mmc
ms.assetid: 7893b3d6-f576-41cc-bbe5-2fcef7c327d7
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: IComponentData interface [MMC],Initialize method, IComponentData.Initialize, IComponentData::Initialize, Initialize, Initialize method [MMC], Initialize method [MMC],IComponentData interface, _slate_icomponentdata_initialize, mmc.icomponentdata_initialize, mmc/IComponentData::Initialize
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
 - IComponentData.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IComponentData::Initialize


## -description


The <b>IComponentData::Initialize</b> method provides an entry point to the console.


## -parameters




### -param pUnknown [in]

A pointer to the console IUnknown interface. This interface pointer can be used to call QueryInterface for 
<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a> and 
<a href="https://msdn.microsoft.com/894f99a6-2189-458d-a50f-497930d4a9dd">IConsoleNameSpace2</a>.


## -returns



This method can return one of these values.




## -remarks



<b>IComponentData::Initialize</b> is called when a snap-in is created and has items to enumerate in the scope pane. The pointer to <a href="https://msdn.microsoft.com/library/ms680509(v=VS.85).aspx">IUnknown</a> that is passed in is used to make <a href="https://msdn.microsoft.com/library/ms682521(v=VS.85).aspx">QueryInterface</a> calls to the console for interfaces such as 
<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a> and 
<a href="https://msdn.microsoft.com/894f99a6-2189-458d-a50f-497930d4a9dd">IConsoleNamespace2</a>. The snap-in should also call 
<a href="https://msdn.microsoft.com/b5cc356f-c8ea-4c4f-b643-3bfb6d7fb15b">IConsole2::QueryScopeImageList</a> to get the image list for the scope pane and add images to be displayed on the scope pane side.




## -see-also




<a href="https://msdn.microsoft.com/65eaa5ef-182b-4fec-bb3d-a308ac9dc660">IComponent</a>



<a href="https://msdn.microsoft.com/60900b8d-59cc-4c1d-86b7-b902ba89216d">IComponentData</a>



<a href="https://msdn.microsoft.com/9a20d09d-219c-4bcb-95b3-67a44e41629e">IConsole2</a>
 

 

