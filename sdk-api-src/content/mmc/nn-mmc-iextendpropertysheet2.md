---
UID: NN:mmc.IExtendPropertySheet2
title: IExtendPropertySheet2
author: windows-sdk-content
description: The IExtendPropertySheet2 interface is introduced in MMC 1.1.
old-location: mmc\iextendpropertysheet2.htm
tech.root: mmc
ms.assetid: 9beb0a0a-b3bf-46d0-b10c-0fc3ab25c18d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IExtendPropertySheet2, IExtendPropertySheet2 interface [MMC], IExtendPropertySheet2 interface [MMC],described, _slate_iextendpropertysheet2, mmc.iextendpropertysheet2, mmc/IExtendPropertySheet2
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
 - IExtendPropertySheet2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExtendPropertySheet2 interface


## -description


The 
<b>IExtendPropertySheet2</b> interface is introduced in MMC 1.1.

The 
<b>IExtendPropertySheet2</b> interface enables a snap-in component to add pages to the property sheet of an item.

<b>IExtendPropertySheet2</b> supersedes the <b>IExtendPropertySheet</b> interface for MMC 1.1. In addition to inheriting all of the methods of <b>IExtendPropertySheet</b>, 
<b>IExtendPropertySheet2</b> has the following method:


<a href="https://msdn.microsoft.com/caecb35a-3f59-4a04-af46-862ded9685cf">IExtendPropertySheet2::GetWatermarks</a>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IExtendPropertySheet2</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IExtendPropertySheet2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IExtendPropertySheet2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">CreatePropertyPages</a>
</td>
<td align="left" width="63%">
Adds pages to a property sheet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/caecb35a-3f59-4a04-af46-862ded9685cf">GetWatermarks</a>
</td>
<td align="left" width="63%">
Gets the watermark and header bitmap for the Wizard 97 style.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17d45a0b-a0cc-407e-815f-0e733c988d69">QueryPagesFor</a>
</td>
<td align="left" width="63%">
Determines whether the object needs pages.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b41508bf-8399-44bb-abad-754aa5d32776">Adding Property Pages and Wizard Pages</a>
 

 

