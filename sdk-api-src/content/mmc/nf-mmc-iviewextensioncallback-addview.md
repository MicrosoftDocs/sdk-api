---
UID: NF:mmc.IViewExtensionCallback.AddView
title: IViewExtensionCallback::AddView
author: windows-sdk-content
description: Adds a view to the result pane.
old-location: mmc\iviewextensioncallback_addview.htm
tech.root: mmc
ms.assetid: 3e794787-d328-4cbf-822e-8846fed81a57
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddView, AddView method [MMC], AddView method [MMC],IViewExtensionCallback interface, IViewExtensionCallback interface [MMC],AddView method, IViewExtensionCallback.AddView, IViewExtensionCallback::AddView, _slate_iviewextensioncallback_addview, mmc.iviewextensioncallback_addview, mmc/IViewExtensionCallback::AddView
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
req.lib: Mmc.lib
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
 - IViewExtensionCallback.AddView
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IViewExtensionCallback::AddView


## -description


The 
AddView method adds a view to the result pane. This method is implemented by MMC and is called by view extensions. For more information, see 
<a href="https://msdn.microsoft.com/3c626853-a9f1-4961-97d0-a12d0bf8b9ed">Extending Views</a>.


## -parameters




### -param pExtViewData [in]

A pointer to an 
<a href="https://msdn.microsoft.com/8396e786-a0ea-4ff8-b899-a23e6552aa92">MMC_EXT_VIEW_DATA</a> structure, which contains information about the view being added to the result pane. The bReplacesDefaultView member of the 
<b>MMC_EXT_VIEW_DATA</b> structure determines if the standard view is removed when adding the new view.


## -returns



If successful, the return value is S_OK. Other return values indicate an error code.




## -see-also




<a href="https://msdn.microsoft.com/3c626853-a9f1-4961-97d0-a12d0bf8b9ed">Extending Views</a>



<a href="https://msdn.microsoft.com/a6ea8735-4cad-4c04-be97-dfad01b00388">IExtendView</a>



<a href="https://msdn.microsoft.com/447b51b1-e206-43c8-8536-049c831dedb7">IExtendView::GetViews</a>



<a href="https://msdn.microsoft.com/8396e786-a0ea-4ff8-b899-a23e6552aa92">MMC_EXT_VIEW_DATA</a>



<a href="https://msdn.microsoft.com/410f8a6a-7df2-4610-97e9-108e185d52a6">View Extension Mechanism</a>
 

 

