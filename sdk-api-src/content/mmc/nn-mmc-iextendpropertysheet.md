---
UID: NN:mmc.IExtendPropertySheet
title: IExtendPropertySheet
author: windows-sdk-content
description: Enables a snap-in component to add pages to the property sheet of an item.
old-location: mmc\iextendpropertysheet.htm
old-project: MMC
ms.assetid: BE0AD832-0FF0-44ED-BD11-3F9BD2860DE5
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IExtendPropertySheet, IExtendPropertySheet interface [MMC], IExtendPropertySheet interface [MMC],described, mmc.iextendpropertysheet, mmc/IExtendPropertySheet
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
req.idl: Mmc.idl
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
 - IExtendPropertySheet
product: Windows
targetos: Windows
req.lib: Mmc.lib
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IExtendPropertySheet interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables a snap-in component to add pages to the property sheet of an item.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendPropertySheet</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExtendPropertySheet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtendPropertySheet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8B99EC8D-AFE1-4944-AF61-BFE93C0AF7DE">CreatePropertyPages</a>
</td>
<td align="left" width="63%">
Adds pages to a property sheet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Mt300856(v=VS.85).aspx">QueryPagesFor</a>
</td>
<td align="left" width="63%">
Determines whether the object needs pages.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b41508bf-8399-44bb-abad-754aa5d32776">Adding Property Pages and Wizard Pages</a>



<a href="https://msdn.microsoft.com/c95742a4-ae9b-40f3-8d88-c4955e5a3032">MMC 2.0 Interfaces and Methods</a>
 

 

