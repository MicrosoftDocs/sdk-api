---
UID: NN:mmc.IViewExtensionCallback
title: IViewExtensionCallback (mmc.h)
author: windows-sdk-content
description: The IViewExtensionCallback interface is used to add a view to the result pane.
old-location: mmc\iviewextensioncallback.htm
tech.root: mmc
ms.assetid: 1854ab01-e518-4ff4-a1d5-d1e03b348992
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IViewExtensionCallback, IViewExtensionCallback interface [MMC], IViewExtensionCallback interface [MMC],described, _slate_iviewextensioncallback, mmc.iviewextensioncallback, mmc/IViewExtensionCallback
ms.topic: interface
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
 - IViewExtensionCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IViewExtensionCallback interface


## -description


The 
<b>IViewExtensionCallback</b> interface is used to add a view to the result pane. During the call to the view extension's 
<a href="https://msdn.microsoft.com/447b51b1-e206-43c8-8536-049c831dedb7">IExtendView::GetViews</a> method, MMC provides an <b>IViewExtensionCallback</b> interface pointer; this pointer is valid only during the call and should not be saved for later use.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IViewExtensionCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IViewExtensionCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IViewExtensionCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e794787-d328-4cbf-822e-8846fed81a57">AddView</a>
</td>
<td align="left" width="63%">
Adds a view to the result pane, and optionally removes the standard view.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3c626853-a9f1-4961-97d0-a12d0bf8b9ed">Extending Views</a>



<a href="https://msdn.microsoft.com/a6ea8735-4cad-4c04-be97-dfad01b00388">IExtendView</a>



<a href="https://msdn.microsoft.com/447b51b1-e206-43c8-8536-049c831dedb7">IExtendView::GetViews</a>



<a href="https://msdn.microsoft.com/410f8a6a-7df2-4610-97e9-108e185d52a6">View Extension Mechanism</a>
 

 

