---
UID: NF:mmc.IExtendView.GetViews
title: IExtendView::GetViews (mmc.h)
author: windows-sdk-content
description: The GetViews method retrieves information about the extended view and adds extended views to the result pane.
old-location: mmc\iextendview_getviews.htm
tech.root: mmc
ms.assetid: 447b51b1-e206-43c8-8536-049c831dedb7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetViews, GetViews method [MMC], GetViews method [MMC],IExtendView interface, IExtendView interface [MMC],GetViews method, IExtendView.GetViews, IExtendView::GetViews, _slate_iextendview_getviews, mmc.iextendview_getviews, mmc/IExtendView::GetViews
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
 - IExtendView.GetViews
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExtendView::GetViews


## -description


The 
GetViews method retrieves information about the extended view and adds extended views to the result pane.

View extensions use the 
<a href="https://msdn.microsoft.com/1854ab01-e518-4ff4-a1d5-d1e03b348992">IViewExtensionCallback</a> interface methods to provide information about the extended view. A pointer to the 
IViewExtensionCallback interface is provided as a parameter of the <b>IExtendView::GetViews</b> method.


## -parameters




### -param pDataObject [in]

A pointer to the snap-in data object.


### -param pViewExtensionCallback [in]

A pointer to the 
<a href="https://msdn.microsoft.com/1854ab01-e518-4ff4-a1d5-d1e03b348992">IViewExtensionCallback</a> interface. The view extension snap-in uses the 
IViewExtensionCallback interface to add information about the extended view. The snap-in can also call the 
<a href="https://msdn.microsoft.com/3e794787-d328-4cbf-822e-8846fed81a57">IViewExtensionCallback::AddView</a> method multiple times to add multiple extended views. The value in pViewExtensionCallback is valid only during the call to <b>IExtendView::GetViews</b>; view extension snap-ins must not save this pointer for later use.


## -returns



If successful, the return value is S_OK. Other return values indicate an error code.




## -remarks



For more information and a C++ code example for <b>IExtendView::GetViews</b>, see 
<a href="https://msdn.microsoft.com/9c4c936e-f74a-4fbf-bd32-aa78ebb6da6e">Extending a Primary Snap-in's View</a>.




## -see-also




<a href="https://msdn.microsoft.com/3c626853-a9f1-4961-97d0-a12d0bf8b9ed">Extending Views</a>



<a href="https://msdn.microsoft.com/9c4c936e-f74a-4fbf-bd32-aa78ebb6da6e">Extending a Primary Snap-in's View</a>



<a href="https://msdn.microsoft.com/1854ab01-e518-4ff4-a1d5-d1e03b348992">IViewExtensionCallback</a>



<a href="https://msdn.microsoft.com/3e794787-d328-4cbf-822e-8846fed81a57">IViewExtensionCallback::AddView</a>
 

 

