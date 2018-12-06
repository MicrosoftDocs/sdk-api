---
UID: NN:mmc.IPropertySheetCallback
title: IPropertySheetCallback
author: windows-sdk-content
description: The IPropertySheetCallback interface is a COM-based interface used by a snap-in to add its property pages to a property sheet.
old-location: mmc\ipropertysheetcallback.htm
tech.root: mmc
ms.assetid: e2115929-692e-4e59-bcdb-f37b02c53224
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPropertySheetCallback, IPropertySheetCallback interface [MMC], IPropertySheetCallback interface [MMC],described, _slate_ipropertysheetcallback, mmc.ipropertysheetcallback, mmc/IPropertySheetCallback
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPropertySheetCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertySheetCallback interface


## -description


The 
<b>IPropertySheetCallback</b> interface is a COM-based interface used by a snap-in to add its property pages to a property sheet.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPropertySheetCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPropertySheetCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPropertySheetCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db19fc38-7111-42f2-83a9-a08473a4d49b">AddPage</a>
</td>
<td align="left" width="63%">
Enables the snap-in to add a page to a property sheet.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2d54efbd-d88e-430e-9e46-c2b80559d356">RemovePage</a>
</td>
<td align="left" width="63%">
Enables the snap-in to remove a page from a property sheet.

</td>
</tr>
</table> 

