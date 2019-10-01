---
UID: NN:mmc.IExtendPropertySheet
title: IExtendPropertySheet (mmc.h)
author: windows-sdk-content
description: Enables a snap-in component to add pages to the property sheet of an item.
old-location: mmc\iextendpropertysheet.htm
tech.root: mmc
ms.assetid: BE0AD832-0FF0-44ED-BD11-3F9BD2860DE5
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExtendPropertySheet, IExtendPropertySheet interface [MMC], IExtendPropertySheet interface [MMC],described, mmc.iextendpropertysheet, mmc/IExtendPropertySheet
ms.topic: interface
f1_keywords: 
 - "mmc/IExtendPropertySheet"
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
 - IExtendPropertySheet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExtendPropertySheet interface


## -description


<div class="alert"><b>Note</b>  This interface is obsolete, and only used in MMC 1.0.</div><div> </div>Enables a snap-in component to add pages to the property sheet of an item.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendPropertySheet</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IExtendPropertySheet</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendpropertysheet-createpropertypages">CreatePropertyPages</a>
</td>
<td align="left" width="63%">
Adds pages to a property sheet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iextendpropertysheet-querypagesfor">QueryPagesFor</a>
</td>
<td align="left" width="63%">
Determines whether the object needs pages.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/adding-property-pages-and-wizard-pages">Adding Property Pages and Wizard Pages</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mmc/mmc-interfaces-and-methods">MMC 2.0 Interfaces and Methods</a>
 

 

