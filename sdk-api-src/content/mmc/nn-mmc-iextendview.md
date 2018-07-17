---
UID: NN:mmc.IExtendView
title: IExtendView
author: windows-sdk-content
description: The IExtendView interface provides information about the extended view.
old-location: mmc\iextendview.htm
old-project: mmc
ms.assetid: a6ea8735-4cad-4c04-be97-dfad01b00388
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: IExtendView, IExtendView interface [MMC], IExtendView interface [MMC],described, _slate_iextendview, mmc.iextendview, mmc/IExtendView
ms.prod: windows
ms.technology: windows-sdk
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
 - IExtendView
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IExtendView interface


## -description


The 
<b>IExtendView</b> interface provides information about the extended view.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendView</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExtendView</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtendView</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/447b51b1-e206-43c8-8536-049c831dedb7">GetViews</a>
</td>
<td align="left" width="63%">
Returns the extended view information. MMC calls this method so that a view extension snap-in can add extended views to the result pane.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/a6ea8735-4cad-4c04-be97-dfad01b00388">IExtendView</a>



<a href="https://msdn.microsoft.com/1854ab01-e518-4ff4-a1d5-d1e03b348992">IViewExtensionCallback</a>



<a href="https://msdn.microsoft.com/410f8a6a-7df2-4610-97e9-108e185d52a6">View Extension Mechanism</a>
 

 

